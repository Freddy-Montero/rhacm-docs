---

copyright:
  years: 2019
lastupdated: "2019-12-05"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Deploying application resources with a rolling update

If you want to roll out an update for a subscription<!-- or deployable--> to your managed clusters, you can configure the deployment to occur on only a percentage of your managed clusters at a time. When the deployment on those clusters is successful, the deployment is rolled out incrementally to the remaining clusters.
{:shortdesc}

When you run a percentage rollout, the rolling update happens on only the specified percentage of clusters. As the deployment completes on one cluster, the deployment begins on another cluster while maintaining the percentage of clusters that are made unavailable. If an error occurs during the deployment to one cluster, the deployment to that cluster is stopped. The cluster remains unavailable until the error is resolved and the deployment can complete on that cluster. Meanwhile, the overall deployment continues on the remaining clusters. The cluster or clusters where an error occurred are still counted towards the percentage of clusters where the rolling update occurs. If the number of clusters where occurred matches the specified percentage for the rolling update, the overall rollout for the deployment is stopped until the errors are resolved.

With a percentage rollout, you can phase in a deployment to your clusters to find any bugs or issues during the rollout before the deployment begins on all clusters. For instance, you can use a percentage rollout when you need to deploy a patch to your clusters. You can start your deployment with a rollout of the patch to 10% of your clusters to view the success of the deployment as the rolling update occurs. When the deployment is successful on a cluster, the deployment continues to another cluster to reach the 10% of clusters until the overall deployment reaches 100% completion. By limiting the deployment to only a percentage of clusters you can determine earlier whether a deployment is failing and stop the deployment to correct any issues.

The rolling update for a deployment runs on the Hub cluster. The deployment rollout occurs for the managed cluster namespaces that exist on the Hub cluster. When the rolling update is completed, the updates can be propagated to the actual managed clusters, such as by using an existing subscription for each managed cluster. The managed cluster namespaces that are updated are defined by the placement rule for the subscription or deployable.

### About this task

You can configure a percentage rollout for a subscription or directly for a deployable resource.

  - [Configuring a rolling update for a subscription](#subsription_rollout)
  - [Examples](#example_rollout)
<!--  - [Configuring a rolling update for a deployable](#deployable_rollout) -->

A rolling update for a subscription <!-- or deployable-->uses the rolling update feature that is included in the Kubernetes resource definition. To configure this feature for a deploying a subscription or deployable, you need to create or update the following Kubernetes resources:

1. The initial subscription or deployable resource.
  
    This resource is used to define and deploy the initial resource that later updated through the rolling update. As part of the definition for this initial resource, you need to identify that a rolling update is used for deploying updates. You also need to identify the percentage of clusters to be updated at a time, the associated target resource, and the placement rule that identifies the target clusters.

2. The target subscription or deployable resource.  

    This resource defines the version of the subscription or deployable that is being deployed through the rolling update.

3. The placement rule for the initial subscription or deployable resource.

    This placement rule identifies the clusters where the initial and target resource is deployed. The rolling update does not target any clusters that are not defined by the placement rule.  
    **Note:** This placement rule must be associated with only the initial resource. The rolling update uses only the placement rule that is associated with the initial resource. Do not include parameters in the target subscription or deployable resource to associate that resource with a placement rule.

### Limitations and known issues

- For a deployable rolling update, the initial and target deployable must be included within the same channel.
- Target subscriptions and target deployables cannot define any placement rule. The initial subscription or initial deployable must define the placement rule for the rolling update.

## Configuring a rolling update for a subscription
{: #subsription_rollout}

If you have existing subscriptions that you want to configure to use a rolling update, you need to create your target subscription and update your initial existing subscription to include the required annotations. 

### Prerequisites

- You have an initial subscription that points to the initial version of a Kubernetes resource or Helm chart and a placement rule for defining the resource or chart deployment.

   This initial subscription serves as the channel subscription and includes the settings for defining the channel and package information for the subscription.

   For more information about how to define a subscription, see [Creating and managing subscriptions](managing_subscriptions.md).

   For more information about how to define a placement rule, see [creating and managing placement rules](managing_placement_rules.md).

- The subscription that points to the initial resource or chart version is deployed to your target managed clusters and has been used to deploy the initial version of the resource or chart to the same target managed clusters.

At this stage no rolling update is configured and any change to the initial version at the source is then deployed to all managed clusters.

### Procedure

1. Create the target subscription resource YAML definition to point to the newer version of the resource or chart to deploy. This definition must use the same definition structure as any subscription application resource kind. However, this target subscription must not include the annotations for defining a rolling update and must not define any placement rule.

2. Update the initial subscription YAML definition to Include the following annotations to indicate that a rolling update is used for updating the subscription:

   ```yaml
   annotations:
     app.ibm.com/rollingupdate-target:
     app.ibm.com/rollingupdate-maxunavailable:
   ```
   {: codeblock}

   - The `app.ibm.com/rollingupdate-target` annotation identifies the target subscription.
   - The `app.ibm.com/rollingupdate-maxunavailable` annotation identifies the maximum percentage of clusters that can be deployed at a time and rendered unavailable during the update. The actual number of clusters is determined by rounding down to an absolute value. By default, the maximum percentage is 25%.
   - The definition does not include any other configurations for the managing the rolling update.

   For example, the following snippet of a YAML definition shows sample values for these annotations:

   ```yaml
   metadata:
   annotations:
       app.ibm.com/rollingupdate-target: target-subscription-name
       app.ibm.com/rollingupdate-maxunavaialble: 30
   name: initial-subscription-name
   namespace: default
   ```
   {: codeblock}

   In the preceding example, the rolling update includes 30% of clusters.

   You can use the Kubernetes CLI (kubectl) tool to add the annotations to an existing subscription instead of directly modifying the YAML definition. Use the following command to add the annotations to a subscription:

   ```yaml
   kubectl annotate --overwrite subscriptions.app.ibm.com initial-subscription-name -n default app.ibm.com/rollingupdate-target=target-subscription-name app.ibm.com/rollingupdate-maxunavaialble=30
   ```
   {: codeblock}

For example definitions of resources that use a rolling update, see [Examples](#example_rollout).

With the subscription resources created or updated, the rolling update begins and the new target subscription and updated initial subscription are deployed to the managed clusters. Then, the target subscription that is on the managed clusters is used to detect the new version of the resource or chart for deployment.

<!--
## Configuring a rolling update for a deployable
{: #deployable_rollout}

1. Create or update the resource YAML definition for the initial deployable application resource. This resource is the deployable that is later updated through the rolling update.  

   Use the standard definition structure for any deployable application resource kind to define the deployable. However, you must include the following parameters as part of the YAML definition

   1. Include the following annotations to indicate that a rolling update is used for updating the deployable: 
     ```yaml
     annotations:
       app.ibm.com/rollingupdate-target: 
       app.ibm.com/rollingupdate-maxunavailable: 
     ```
     {: codeblock}

     - The `app.ibm.com/rollingupdate-target` annotation identifies the target deployable. 
     - The `app.ibm.com/rollingupdate-maxunavailable` annotation identifies the maximum percentage of clusters that can be deployed at a time and rendered unavailable during the update. The actual number of clusters is determined by rounding down to an absolute value. By default, the maximum percentage is 25%.
     - The definition does not include any other configurations for the managing the rolling update.

     For example, the following snippet of a YAML definition shows sample values for these annotations: 
     ```yaml
     metadata:
     annotations:
         app.ibm.com/rollingupdate-target: target-deployable-name
         app.ibm.com/rollingupdate-maxunavaialble: 30
         app.ibm.com/is-local-deployable: "false"
     name: initial-deployable-name
     namespace: default
     ```
     {: codeblock}

     In the preceding example, the rolling update includes 30% of clusters. 

   2. Include the fields to define the placement rule for deploying this initial deployable and for deploying the target deployable.
     ```yaml
     spec: 
      placement:
        placementRef:
          kind: PlacementRule
          name: placement-rule-name
      ```
      {: codeblock}

      - The `spec.placement.placementRef.name` field identifies the name of the placement rule for deploying the initial and target deployables.
      - The `spec.placement.placementRef.kind` field indicates that the named resource is a placement rule. This value must be set to `PlacementRule`.

2. Create the resource YAML definition for the target deployable. This definition must use the same definition structure as any deployable application resource kind. However, this target deployable must not include the annotations for defining a rolling update and must not define any placement rule. 

3. Create or update the placement rule for the initial and target subscription. This definition must use the same definition structure as any placement rule application resource kind.

For example, definitions for these resources, see [Examples](#example_rollout).

For more information about how to define a deployable, see [Creating and managing deployables](managing_deployables.md).

For more information about how to define a placement rule, see [creating and managing placement rules](managing_placement_rules.md).
-->

## Example
{: #example_rollout}

The following example YAML definitions show the required fields for deploying an update for a deployable by using a rolling update.

- The following definitions create a `development-ns/development-ns` namespace and `development-ch` channel to use for the deployables and subscriptions:

```yaml
---
apiVersion: v1
kind: Namespace
metadata:
  name: development-ns
---
apiVersion: app.ibm.com/v1alpha1
kind: Channel
metadata:
  name: development-ch
  namespace: development-ns
spec:
    type: Namespace
    pathname: development-ns
```
{: codeblock}

- The following definitions create the initial deployable resource and the updated version of that deployable. Both of these deployable resources are configMap templates as an example.

```yaml
---
apiVersion: app.ibm.com/v1alpha1
kind: Deployable
metadata:
  annotations:
    app.ibm.com/is-local-deployable: "false"
    app.ibm.com/deployable-version: 1.2.3
  name: configmap-initial
  namespace: development-ns
spec:
  template:
    apiVersion: v1
    kind: ConfigMap
    metadata:
      labels:
        app: my-application
      name: development-ns
      namespace: default
    data:
      purpose: For testing purposes
---
apiVersion: app.ibm.com/v1alpha1
kind: Deployable
metadata:
  annotations:
    app.ibm.com/is-local-deployable: "false"
    app.ibm.com/deployable-version: 1.2.4
  name: configmap-update
  namespace: development-ns
spec:
  template:
    apiVersion: v1
    kind: ConfigMap
    metadata:
      labels:
        app: my-application
      name: development-ns
      namespace: default
    data:
      purpose: For testing a rolling update
```
{: codeblock}

- The following YAML content includes the definition for the initial subscription to the channel and initial deployable. This YAML content also includes the definition for the target subscription to the channel for rolling out the updated deployable. The definition for the initial subscription also includes the `placement` definition to list the target clusters where the deployables must be placed instead of referencing an associated placement rule.

```yaml
apiVersion: app.ibm.com/v1alpha1
kind: Subscription
metadata:
  name: subscription-initial
  namespace: default
spec:
  channel: development-ns/development-ns
  packageFilter:
    version: "=1.2.3"
  placement:
    clusters:
    - name: cluster138
    - name: cluster140
    - name: cluster50
    - name: cluster51
    - name: cluster52
---
apiVersion: app.ibm.com/v1alpha1
kind: Subscription
metadata:
  name: subscription-target
  namespace: default
spec:
  channel: development-ns/development-ns
  packageFilter:
    version: "=1.2.4"
```
{: codeblock}

The definition for the initial subscription does not include the required fields for using a rolling update:

```yaml
app.ibm.com/rollingupdate-maxunavaialble: 20
app.ibm.com/rollingupdate-target: subscription-target
```
{: codeblock}

These annotations can be added to the initial subscription with the following command:

```yaml
kubectl annotate --overwrite subscriptions.app.ibm.com subscription-initial -n default app.ibm.com/rollingupdate-target=subscription-target app.ibm.com/rollingupdate-maxunavaialble=20
```
{: codeblock}

With the annotations added, the definition for the initial subscription resembles the following YAML content:

```yaml
apiVersion: app.ibm.com/v1alpha1
kind: Subscription
metadata:
  annotations:
    app.ibm.com/rollingupdate-maxunavaialble: 20
    app.ibm.com/rollingupdate-target: subscription-target
  name: subscription-initial
  namespace: default
spec:
  channel: development-ns/development-ns
  packageFilter:
    version: "=1.2.3"
  placement:
    clusters:
    - name: cluster138
    - name: cluster140
    - name: cluster50
    - name: cluster51
    - name: cluster52
```
{: codeblock}

<!--
### Example 2: Rolling out a deployable resource
 - Target deployable YAML definition
    ```yaml
    apiVersion: app.ibm.com/v1alpha1
    kind: Deployable
    metadata:
      annotations:
        app.ibm.com/is-local-deployable: "false"
      name: target-deployable-A
      namespace: default
    spec:
      template:
        apiVersion: apps/v1
        kind: Deployment
        metadata:
          namespace: default
    ```
    {: codeblock}
-->
