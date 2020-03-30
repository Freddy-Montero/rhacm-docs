---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-17"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Log in to Red Hat Advanced Cluster Management for Kubernetes console causes default backend 404 error from IBM Kubernetes Service

An error appears when you log in to the Red Hat Advanced Cluster Management for Kubernetes console because of a connection reuse problem.

## Symptom

A `default backend - 404` error is displayed in the browser when you attempt to log in.

## Causes

an `HTTP/2` connection reuse, also called `HTTP/2 keep-alive` causes the problem.

Environment: OpenShift 3.11 on IBM Kubernetes Service.

## Solution

1. Add `use-http2: "false"` to the `nginx-ingress-controller` ConfigMap in kube-system. Run the following command:

```
oc edit configmap -n kube-system nginx-ingress-controller
```
{: codeblock}

2. Add the following flag and value to the `data` section:

```
use-http2: "false"
```
{: codeblock}

3. Restart the pod to get the latest configuration from the ConfigMap:
 
```
kubectl -n kube-system delete pods $(kubectl -n kube-system -l app=nginx-ingress-controller -l component=nginx-ingress-controller get pods | grep -v NAME | awk '{print $1}')
```
{: codeblock}