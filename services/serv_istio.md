---	

copyright:	
  years: 2019, 2020	
lastupdated: "2020-03-26"	

---	

# Enabling an Istio service for discovery

You can configure the Red Hat Advanced Cluster Management for Kubernetes service registry to discover Istio services that are in different Red Hat Advanced Cluster Management for Kubernetes managed clusters.	

When you have multiple instances of an Istio service that are managed by Red Hat Advanced Cluster Management for Kubernetes, it is challenging to maintain them. The Red Hat Advanced Cluster Management for Kubernetes service discovery function discovers Istio services that are configured to be discovered.	

**Required user type or access level:** Cluster administrator.

The plug-in for the Istio discovery must be enabled when you import your target managed cluster if you want to discover an Istio service in your managed clusters.

**Note:** If you enable the Istio plug-in, you need to install the [Multicluster service mesh](https://istio.io/docs/concepts/multicluster-deployments/#multicluster-service-mesh). The mesh must include individually deployed Istio control planes in every cluster and must use gateways to connect services across clusters.

## Discover the Istio service

To discover an Istio service within the managed clusters, complete the following steps:

1. Add a service discovery annotation to the Istio service. You must add the annotation to your Istio service definition YAML file for the service that you want to discover.

  ```
  mcm.ibm.com/service-discovery	
  ```

  The following example shows how to add the annotation to the service definition YAML file:	

  ```	
  apiVersion: v1	
  kind: Service	
  metadata:	
   annotations:	
     mcm.ibm.com/service-discovery: "{}"	
   name: dbservice	
   namespace: database	
  spec:	
   ports:	
   - name: http	
      nodePort: 8080	
      port: 8000	
      protocol: TCP	
   selector:	
     app: dbservice	
  ```

2. By default, the annotated service can be discovered on all managed clusters. If you want to discover the service on specific managed clusters, add `target-clusters` in the annotation, as shown in the following example:

  ```
  mcm.ibm.com/service-discovery: '{"target-clusters": ["cluster1", "cluster2"]}'
  ```

3. Access the discovered service by using the service hostname. In this example, the hostname is `dbservice.database`.
