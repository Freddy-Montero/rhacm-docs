---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-19"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Enabling a Kubernetes ingress for discovery

You can configure the Red Hat Advanced Cluster Management for Kubernetes service registry to discover Kubernetes ingresses that are on different Red Hat Advanced Cluster Management for Kubernetes managed clusters.
{: shortdesc}

When you have multiple Kubernetes ingresses that are managed by Red Hat Advanced Cluster Management for Kubernetes, it is challenging to maintain them. The Red Hat Advanced Cluster Management for Kubernetes service discovery function discovers Kubernetes ingresses that are configured to be discovered.

**Required user type or access level:** Cluster administrator.

The plugin for the Kubernetes ingress discovery must be enabled when you import your target managed cluster if you want to discover a Kubernetes ingress in your managed clusters.

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

  **Tip:** You can append the service registry DNS suffix (mcm.svc) to your ingress host name, then you can access the ingress host directly using the host name.

2. By default, the annotated ingress can be discovered on all managed clusters. If you want to discover the service on specific managed clusters, add the `target-clusters` in the annotation, as shown in the following example:

  ```
  mcm.ibm.com/service-discovery: '{"target-clusters": ["cluster1", "cluster2"]}'
  ```
  {: codeblock}

3. Access the discovered ingress by using the ingress host name. In this example, the host name is `mydb.database.mcm.svc`.
