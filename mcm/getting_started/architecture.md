---

copyright:
  years: 2018, 2019
lastupdated: "2019-12-11"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Multicluster architecture

{{site.data.keyword.cloud_pak_mcm}} consists of several multicluster components, which are used to access and manage your clusters. Learn more about the following components for {{site.data.keyword.cloud_pak_mcm}}:

  <img src="../../images/hub_managed.svg" width="50%" alt="Major common components of the hub cluster and managed cluster">

  - [Hub cluster](#hub)
  - [Managed cluster](#managed)
  - [Application resources](#app)
  - [Governance and risk](#policy)

## Hub cluster
{: #hub}

The hub cluster is the common term that is used to define the central controller that runs in an {{site.data.keyword.cloud_pak_mcm}} cluster.

The hub cluster aggregates information from multiple clusters by using an asynchronous work request model. With a graph database, the hub cluster maintains the state of clusters and applications that run on it. The hub cluster also uses `etcd`, a distributed key value store, to store the state of work requests and results from multiple clusters and provides a set of REST APIs for the various functions that it supports.

## Managed cluster
{: #managed}

The managed cluster is used to define the {{site.data.keyword.cloud_pak_mcm}} {{site.data.keyword.klust}}, which is the agent that is responsible for a single Kubernetes cluster. The managed cluster initiates a connection to the hub cluster, receives work requests, applies work requests, then returns the results. The managed cluster connects to various services within the cluster for operations, including the Kubernetes API service, the Tiller service (Helm), and Weave for topology.


See [Managing your clusters with {{site.data.keyword.cloud_pak_mcm}}](../manage_cluster/intro.md) for configuration and import information.

## Application resources
{: #app}

After you configure an {{site.data.keyword.cloud_pak_mcm}} hub cluster and a managed cluster, you can view and deploy applications with application resources. Your _Application_ is used to only _view_ your resource, while other application resource examples are for deployment. A multi-cluster application uses a Kubernetes specification, but with additional automation of the deployment and lifecycle management of resources to individual clusters.

See [Managing applications](../applications/overview.md) for more application topics.

## Governance and risk
{: #policy}

After you configure an {{site.data.keyword.cloud_pak_mcm}} hub cluster and a managed cluster, you can define {{site.data.keyword.cloud_pak_mcm}} security risk and create policies with templates from the _Governance and risk_ page. For more information see, [{{site.data.keyword.cloud_pak_mcm}} Governance and risk](../compliance/compliance_intro.md).

See [{{site.data.keyword.cloud_pak_mcm}} installation](../../install/overview.md) to prepare your cluster and get configuration information.
