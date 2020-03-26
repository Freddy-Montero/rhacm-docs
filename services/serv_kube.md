---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-26"

---

# Enabling a Kubernetes service for discovery

You can configure the Red Hat Advanced Cluster Management for Kubernetes service registry to discover Kubernetes services that are in different Red Hat Advanced Cluster Management for Kubernetes managed clusters. 

A Kubernetes service exposes a group of pods that are running on a managed cluster. The Red Hat Advanced Cluster Management for Kubernetes service discovery function only discovers Kubernetes services that are configured to be discovered. 

**Required user type or access level:** Cluster administrator.

## Discover the Kubernetes service

To discover a Kubernetes service on your managed clusters, complete the following steps:

1. Annotate the service to enable the service discovery.

  You must enable the service in the managed cluster to be discovered by adding the following annotation to your service definition for the service that you want to discover:

  ```
  mcm.ibm.com/service-discovery
  ```
  
  The following example shows the format for the `dbservice`:
  
  ```
  apiVersion: v1
  kind: Service
  metadata:
    annotations:
      mcm.ibm.com/service-discovery: "{}"
    name: dbservice
    namespace: database
  spec:
    type: LoadBalancer
    ports:
    - name: http
      nodePort: 8080
      port: 8000
      protocol: TCP
    selector:
      app: dbservice
  ```

  **Note:** The Kubernetes service that you want to discover must be either a `LoadBalancer` or `NodePort` type.

2. By default, the annotated service can be discovered on all managed clusters. If you want to discover the service on specific managed clusters, add `target-clusters` in the annotation, as shown in the following example:

  ```
  mcm.ibm.com/service-discovery: '{"target-clusters": ["cluster1", "cluster2"]}'
  ```

3. Access the discovered service by using the following format:
  
  ```
  <service-name>.<service-namespace>.<service-registry-dns-suffix>
  ```
  
  An example of the format is: `dbservice.database.mcm.svc`.
