---

copyright:
  years: 2020
lastupdated: "2020-04-06"

---

# Deploying application resources

You can deploy application resources, such as Kubernetes deployable objects or Helm charts to a cluster to update existing applications or to add applications. Red Hat Advanced Cluster Management for Kubernetes supports multiple options for the deployment of deployable objects.

Within the Red Hat Advanced Cluster Management for Kubernetes application model, you use deployables (`deployable.apps.open-cluster-management.io`), which are Kubernetes resources that contain templates to wrap other Kubernetes resources or represent Helm releases for deployment. Deployables are used to wrap other resources to prevent actions from being run against the resources by Kubernetes and other controllers before the resources are placed on target clusters. For more information about deployables, see [Application resources](app_resources.md).

When you are preparing to deploy, the deployment option that you can use can depend on the following requirement:
* You are deploying to a single cluster or multiple clusters.
* You need to deploy frequent or infrequent updates.
* You need to configure cluster-specific deployment settings.
* You need to use the same deployment settings for multiple deployables.

In general, if you plan to use a continuous delivery model for developing your applications, use a combination of channels, subscriptions, and placement rules.

* Channels (`channel.apps.open-cluster-management.io`) define a namespace within the Hub cluster and point to a physical place where resources are stored for deployment, such as an object store, Kubernetes namespace, Helm repository, or GitHub repository. Clusters can subscribe to channels for identifying the deployables to deploy to each cluster. Deployables within a channel can be accessed by only the clusters that subscribe to that channel.

* Subscriptions (`subscription.apps.open-cluster-management.io`) are sets of definitions that identify deployables within channels by using annotations, labels, and versions. The subscription operator can monitor the channel for new or updated Helm charts, deployables, or secret. Then, the operator can download the Helm chart, deployable, or secret directly from the source location (Helm repository, GitHub repository, object store, or namespace) to the target managed clusters.

* Placement rules (`PlacementRule.app.ibm.com`) define the target clusters where deployables can be deployed. Use placement rules to help you facilitate the multi-cluster deployment of your deployables.

Channels, subscriptions, and placement rules can help you to unify and simplify your continuous deliveries that involve frequent updates and deployments to multiple clusters. Use a combination of these resources when you need to make deploy to multiple clusters, deploy frequent updates, and share deployment settings across multiple deployables.

If you need to specify placement settings for specific clusters, you can still use shared placement rules and include placement overrides for the deployables that need some different settings. For instance, if you use a placement rule with a deployable that you need to deploy to multiple clusters, you can include overrides for any single cluster than requires some different settings.

If you need to deploy a Kubernetes resource or Helm chart to only a single cluster with infrequent updates, you can use just a placement rule. You can define the placement rule as a separate resource or as part of the definition for the deployable.

Based on your deployment requirements, review the details and process for the following deployment options:

  * [Deploy by using channels, subscriptions, and placement rules](#deploy-by-using-channels-subscriptions-and-placement-rules)
    * [Promote a deployable to a channel](#promote-a-deployable-to-a-channel)
    * [Deploy with a percentage roll out](#deploy-with-a-percentage-roll-out)
  * [Deploy by using only placement rules](#deploy-by-using-only-placement-rules)

## Deploy by using channels, subscriptions, and placement rules

To set up and use channels, subscriptions, and placement rules for deployments, complete the following procedure:

1. If the channel for representing the object store, Kubernetes namespace, or Helm repository does not exist, create the channel. Ensure that you define any labels or annotations that deployables must have before they can be promoted to the channel. For more information, see [Creating and managing channels](managing_channels.md).

2. If your deployables do not exist, create your deployables. For more information, see [Creating and managing deployables](managing_deployables.md).

3. If your target cluster or clusters are not subscribed to the channel, create the subscription. For more information, see [Creating and managing subscriptions](managing_subscriptions.md).

4. Define the placement rule for the deployables that are to be deployed from the channel. For more information, see [Creating and managing placement rules](managing_placement_rules.md).

    A placement rule can be defined for a subscription and for deployables. Define the placement rule or reference to the placement rule in the subscription definition to have the rule apply to multiple deployables and clusters. Define the placement rule or reference to the rule in the deployables definitions when you do not want to have the same settings apply to all deployables for the subscription or when you want to override a subscription-level placement rule. If you are referencing a placement rule, you can also include override settings for a deployable to override some placement rule values with values specific to the deployable.

5. Optional. If you created the placement rule as a stand-alone resource, edit the definition for your subscription or deployables to reference your placement rule.

6. Edit the definition for your deployables and your channel to ensure that deployables are promoted to the channel. For more information, see [Promote a deployable to a channel](#promote_channel).

7. Use the console to monitor the status of the deployment to the target cluster or clusters for the channel.

## Scheduling a deployment

If you need to deploy new or changed Helm charts or other resources during only specific times, you can define subscriptions for those resources to begin deployments during only those specific times. Alternatively, you can restrict deployments from beginning during specific time windows, such as to avoid unexpected deployments during peak business hours.

For more information, see [Scheduling resource deployments for a subscription](managing_subscriptions.md#subscription_timewindow).

## Promote a deployable to a channel

To promote a deployable to a channel, you can use any of the following methods:

* Point the deployable to a specific channel by configuring the `spec.channels` field within the deployable definition with the correct annotations to identify the channel.

    The `spec.channels` parameter is available for deployable (`deployable.apps.open-cluster-management.io`) resources to identify the channels where the deployable is to be promoted. The following example shows a deployable that defines the channels where the deployable is to be included.

    ```yaml
    apiVersion: apps.open-cluster-management.io/v1
    kind: Deployable
    metadata:
        name: deployable1
        namespace: default
      spec:
        template:
        placement:
        overrides:
        dependencies:
        channels:
        - mychannel
        - otherchannel
    ```

* Update the channel definition to identify the deployables to include in the channel. Use the `spec.package` and `spec.packageFilter` fields to specify the deployables.

  As an example, the following channel automatically pull the most recent, or latest, `nginx` chart when a new chart is published to the source Helm repository for the channel. The chart deployable must have a matching version `1.x` to be promoted to the channel.

    ```yaml
    apiVersion: apps.open-cluster-management.io/v1
    kind: Channel
    metadata:
        name: dev
        namespace: dev
    spec:
        type: HelmRepo
        pathname: https://kubernetes-charts.storage.googleapis.com/
    ---
    apiVersion: apps.open-cluster-management.io/v1
    kind: Subscription
    metadata:
        name: mydevsub
        namespace: myspace
    spec:
      channel: ch-dev/dev
      package: nginx
      packageFilter:
        version: 1.x
      placement:
        clusters:
        - name: mydevcluster1
    ```

* Update the subscription definition to identify the deployables. The configuration for promoting a deployable to a channel can also be specified within the subscription definition.

  The following example subscription indicates that the most recent `nginx` version `1.x` chart is to be promoted through the channel for deployment with the subscription.

    ```yaml
    apiVersion: apps.open-cluster-management.io/v1
    kind: Subscription
    metadata:
        name: mydevsub
        namespace: myspace
    spec:
      source: https://kubernetes-charts.storage.googleapis.com/
      package: nginx
      packageFilter:
        version: 1.x
      placement:
        clusters:
        - name: mydevcluster1
    ```

* Update the channel definition to specify channel gate requirements and update the definitions for your deployables to include the fields and values to match the gate requirements.
  
  Channel gate requirements are defined within the `spec.gate` section of a channel definition. If the deployable has the fields to match the channel `spec.gate` values, the deployable is promoted to the channel. In this case, the deployable does not need to point to a specific channel with the  `spec.channels` field.

### Deploy with a percentage roll out  

If you want to roll out a deployment to your target managed clusters instead of deploying to all target cluster, you can configure the deployment of a deployable or chart to only a percentage of your managed clusters at a time. For instance, you might want to roll out a deployment when you need to deploy an update but you do not want to affect all clusters at once. When the deployment is successful on a cluster, the deployment is rolled out to another cluster.

For more information, see [Deploying application resources with rolling update](deployment_rollout.md).

## Deploy by using only placement rules

If you do not want or need to use channels and subscriptions, you can still use placement rules. When you are deploying a deployable by using only a placement rule, the deployable definition can include a reference to a stand-alone placement rule resource.

In this scenario, the placement rule defines how to deploy the deployable on target clusters. This placement rule can also be referenced by other deployables so that those deployables are handled with the same deployment settings.

Alternatively, a deployable can include a placement rule definition within the deployable definition. In this scenario, the deployable does not reference any stand-alone placement rule. The placement rule definition that is defined within a deployable is not referenced and shared by other deployables.

To deploy by using a placement rule, define the placement rule for the deployable either as a stand-alone placement rule resource or as part of the deployable definition. If you define the rule as a separate resource, include the `placementRef` field in the definition for the deployable to point to the placement rule.

For more information about defining a placement rule, see [Creating and managing placement rules](managing_placement_rules.md).
