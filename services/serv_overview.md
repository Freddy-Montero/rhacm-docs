---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-26"

---

# Red Hat Advanced Cluster Management for Kubernetes services overview

A Red Hat Advanced Cluster Management for Kubernetes service can be one of the following types: Kubernetes service, Kubernetes ingress, or Istio service. A Red Hat Advanced Cluster Management for Kubernetes service runs on a single managed cluster or on multiple managed clusters. They support Kubernetes services, Kubernetes ingress services, and Istio services.

The following sections provide a summary of the types of services that are available for Red Hat Advanced Cluster Management for Kubernetes.

## Kubernetes service

A _service_ resource is a Kubernetes service resource. Edit the `metadata` section of your service definition to add the service discovery annotation. The following example shows a Kubernetes service resource:

<!-- CD: Where will you find the YAML for the service? -->

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

## Ingress service

An _Ingress_ service is a Kubernetes ingress that defines the criteria where the services on the managed cluster can communicate with other managed clusters. Edit the `metadata` section of your ingress service definition to add the service discovery annotation. See the following sample of an Ingress service definition: 

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

## Istio service

An Istio _service_ is a Kubernetes service resource. Edit the `metadata` section of your Istio service definition to add the service discovery annotation. See the following sample gateway service:

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

See [Working with Red Hat Advanced Cluster Management for Kubernetes service discovery](working_serv_intro.md) for more information about the services. 
