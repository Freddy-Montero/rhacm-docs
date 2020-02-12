---

copyright:
  years: 2019
lastupdated: "2019-06-07"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Enabling a Kubernetes ingress for discovery

You can configure the {{site.data.keyword.mcm_notm}} service registry to discover Kubernetes ingresses that are on different {{site.data.keyword.mcm_notm}} managed clusters.
{: shortdesc}

When you have multiple Kubernetes ingresses that are managed by {{site.data.keyword.mcm_notm}}, it is challenging to maintain them. The {{site.data.keyword.mcm_notm}} service discovery function discovers Kubernetes ingresses that are configured to be discovered.

**Required user type or access level:** Cluster administrator.

## Enable the kube-ingress discovery plugin

The plugin for the Kubernetes ingress discovery must be enabled if you want to discover a Kubernetes ingress in your managed clusters. Complete the following steps to enable the ingress plugin:

1. Log in to your {{site.data.keyword.cloud_pak_mcm}} {{site.data.keyword.gui}}.

2. Navigate to **Workloads** -> **Helm Releases**.

3. Select your `ibm-klusterlet` release.

4. Expand **All parameters**.

5. In the *Multicloud Manager service registry configuration* section, you can enable the plugin that you want to use by entering it in the **Enabled Plugins** field. Your entry should be comma-separated, like the following example:

  ```
  kube-service,kube-ingress
  ```

## Discover the Kubernetes ingress

To discover a Kubernetes ingress within your managed clusters, complete the following steps:

1. Annotate an ingress with service discovery annotation.

  You must enable the ingress in the managed cluster to be discovered by adding the following annotation to the `yaml` file for the ingress that you want to discover:

  ```
  mcm.ibm.com/service-discovery
  ```
  {: codeblock}

  The following example shows how to add this to the ingress:

  ```
  apiVersion: extensions/v1beta1
  kind: Ingress
  metadata:
    name: dbing
    namespace: database
    annotations:
      mcm.ibm.com/service-discovery: "{}"
  spec:
    rules:
    - host: mydb.database.mcm.svc
      http:
        paths:
        - path: /db
          backend:
           serviceName: dbservice
           servicePort: 8000
  ```

  **Tip:** You can append the service registry DNS suffix (mcm.svc) to your ingress host name, thus you can access the ingress host directly using the host name.

2. If the ingress that you added the discovery annotation to has other applications that depend on it, add the ingress to the application's entry as a deployable dependency.

  The following example shows how to add this dependency:

  ```
  apiVersion: apps.ibm.com/v1alpha1
  kind: Deployable
  metadata:
    name: name1
    namespace: workspace
  spec:
    template:
      apiVersion: extensions/v1beta1
      kind: Deployment
      metadata:
        name: ibm-websphere
        labels:
          app: ibm-websphere
      spec:
        replicas: 1
        selector:
          matchLabels:
            app: ibm-websphere
        template:
          metadata:
            labels:
              app: ibm-websphere
          spec:
            containers:
            - name: ibm-websphere
              image: "registry.ng.bluemix.net/seed/ibm-websphere-sample"
              imagePullPolicy: Always
    dependencies:
    - name: dbing
      namespace: database
      kind: Ingress
      apiGroup: extensions/v1beta1
    placement:
      clusterNames:
      - managed cluster1
  ```

  After applying this deployable, its dependent ingress is automatically discovered in the cluster (`managed cluster1`) in which the application is deployed.

3. Access the discovered ingress by using the ingress host name. In this example, the host name is `mydb.database.mcm.svc`.
