---

copyright:
  years: 2020
lastupdated: "2020-03-02"

---

# What's new in Red Hat Advanced Cluster Management for Kubernetes

Red Hat Advanced Cluster Management for Kubernetes provides visibility of your entire Kubernetes domain with built-in governance and application life-cycle management.

Get an overivew of Red Hat Advanced Cluster Management for Kubernetes from the [Product Welcome page](../about/welcome.md). See the [architecture page](../about/architecture.md) to learn more about major components of the product.

To learn about the Red Hat Advanced Cluster Management for Kubernetes console capabilities, see [Observability in the console](../console/console_intro.md).

## Installation

With operator-based installation, you can install a working Red Hat OpenShift cluster on a configured cloud provide, such as Amazon Web Services, in less than 10 minutes. See [Installing Red Hat Advanced Cluster Management for Kubernetes when connected](../install/install_connected.md) for more information.  
  
## Cluster management

* Create clusters on various Kubernetes cloud service providers. You can provision and manage Red Hat OpenShift Container Platform clusters on selected Kubernetes cloud service providers. See [Creating a cluster with Red Hat Advanced Cluster Management for Kubernetes](../manage_cluster/create.md) for more information. 

* Import existing Kubernetes clusters. Import your existing Kubernetes clusters that are hosted on popular cloud service providers, or on private clouds to manage your clusters conveniently in one place. See [Importing a target managed cluster to the hub cluster](../manage_cluster/import.md) for more information.

* Manage all of your Red Hat OpenShift Container Platform cluster upgrades in one interface. You can upgrade imported and provisioned Red Hat OpenShift Container Platform clusters either individually or in groups by using the console.

## Application management

Deploy and maintain day two operations of business applications distributed across your cluster landscape.
Create and manage applications across environments through channel and subscription-based automation. You can also view your applications and resources from the topology page in the console. For more information, see [Managing applications](../manage_applications/overview.md).


  - Application resources are used to group and view the components across your applications.

  - Deployables are Kubernetes resources that wrap or represent other resources to prevent actions from being run against the resources by Kubernetes and other controllers before the resources are placed on target clusters.

  - Placement rules define where and how Helm charts and deployables are deployed. Use placement rules to help you facilitate multicluster deployments of your deployables.

  - Channels are custom resource definitions that can help you streamline deployments and separate cluster access. Channels define a namespace within the hub cluster and point to a physical place where resources are stored for deployment.
  
  - Subscriptions are Kubernetes resources that serve as sets of definitions for identifying Kubernetes resources (in GitHub, Objectstores, or hub deployables) and Helm charts within channels by using annotations, labels, and versions.

## Security and compliance

With the Governance and risk dashboard, you can view and manage the number of security risks and policy violations in your clusters and applications. Create custom policy controllers to report and validate the compliance of your policies on your cluster. Create and manage the following policy controllers that are installed by default:

* [Certificate policy controller](../governance/cert_policy_ctrl.md)
* [Configuration policy controller](../governance/config_policy_ctrl.md)
* [IAM policy controller](../governance/iam_policy_ctrl.md)

See [Red Hat Advanced Cluster Management for Kubernetes Governance and risk](../governance/compliance_intro.md) to learn more about the dashboard and the policy framework.

As you create policies, use the policy element, `templates` to describe how your resource is defined. For more information about the policy elements, see [Red Hat Advanced Cluster Management for Kubernetes policy overview](../governance/policy_overview.md). 
