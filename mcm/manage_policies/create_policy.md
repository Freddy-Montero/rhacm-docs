---

copyright:
  years: 2016, 2018
lastupdated: "2018-01-04"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Creating a deployment policy

Use policies to specify scaling and resource allocation for a pod.
{:shortdesc}

All users can define a new policy in their namespace. For administrators, the policy is created, by default, in the administrator namespace.

1. From the navigation menu, click **Configuration** > **Scaling Policies**.
2. Click **Create Policy**.
3. Provide the policy details. Provide individual values in the Create Policy window.
    <!--* Click **JSON mode**, and enter the policy definition in JSON format.-->
    1. Provide the policy **Name**.
    2. In the **Scale target** field, enter the name of the application that the policy applies to.
    3. Provide the **Minimum replications** value. The default value is 1.
    4. Enter the **Maximum replications** value. This value is the maximum number of replications that are allowed during a scale up.
    5. Enter the **Target CPU** value. This value is the percentage of the available CPU that the application can allocate. If you do not specify the resource limits for your container, the value is set to unlimited.
4. Click **Create**.

A new policy is displayed on the Scaling Policies home page.

To view detailed policy information, click the policy name.
