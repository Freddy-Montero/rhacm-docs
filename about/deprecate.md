---

copyright:
  years: 2019
lastupdated: "2019-12-11"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Stabilized, deprecated, and removed function

Frequent updates to the product and changes in technology require that some function is deprecated or removed from support. See the following sections for definitions of stabilized, deprecated, and removed function and tables that identify items from these categories.
{:shortdesc}

## Stabilized

A _stabilized_ item is not planned for deprecation or removal from a subsequent release of a product, but is no longer updated or developed. Consider the alternative actions in the _Recommended action_ and details that are provided in a table only if stabilized functions are listed for the current release.

## Deprecated

A _deprecated_ item is supported, but no longer recommended for use and might become obsolete. Consider the alternative actions in the _Recommended action_ and details that are provided in the following table:

Product or category | Affected item | Status | Version | Recommended action | More details and links |
-- | -- | -- | -- | -- | -- |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/getHighestRole` | Deprecated | {{site.data.keyword.cloud_pak}} | Replaced by `GET /idmgmt/identity/api/v1/teams/highestRole` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/getHighestRoleForCRN?crn=<resource crn>` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/highestRole?crn=<resource crn>` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/getTeamResources` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/resources` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/k8resources/getK8Resources` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/resources?resourceType=namespace` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/getTeams` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams` | None available. |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/ldapList` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/directories` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/users/<userId>/getTeamRoleMappings` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/roleMappings` | None available |
APIs - `platform-identity-manager` | `GET /idmgmt/identity/api/v1/service/teamRoleBindings` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by `GET /idmgmt/identity/api/v1/teams/roleMappings? userid=<userId>` | None available |
Internal APIs - `iam-token-service` | `POST /oidc/introspect` </br> `POST /oidc/token` </br> `GET /oidc/keys` | Deprecated | {{site.data.keyword.cloud_pak}}  | Replaced by </br> `POST /iam/oidc/introspect` </br> `POST /iam/oidc/token` </br> `GET /iam/oidc/keys` | Both the deprecated and replaced APIs are available in {{site.data.keyword.cloud_pak}}. The deprecated APIs are planned to be removed in a subsequent release.|
Kubernetes API server | `experimental-encryption-provider-config` parameter | Deprecated | version 3.2.0 | Use the `encryption-provider-config` parameter with version `apiserver.config.k8s.io/v1` instead. | |
Logging| The functionality to install extra logging instances with security disabled| Deprecated | version 3.2.0 | Update insecure logging deployments to the 3.2.0 level and use chart parameters to enable security. | None available |
{{site.data.keyword.product}}  | `mcm-inception` | Deprecated | version 3.2.0 | `mcm-inception` is removed from the {{site.data.keyword.mcm_notm}} server chart | None available |
APIs | V1 Helm REST APIs | Deprecated | version 3.2.1 | Replaced by the V2 Helm REST APIs | [Helm API](../apis/helm_apis.md) |
Mutation advisor (deployed with Vulnerability Advisor) | `va/ui/mlist?access_group=kube-system` | Deprecated | {{site.data.keyword.cloud_pak}} {{site.data.keyword.version_cp}}| |None available|
{: caption="Table 1. Deprecated function" caption-side="top"}

## Removed

A _removed_ item is typically function that was deprecated in previous releases and is no longer available in the product. You must use alternative features as a replacement for the removed function. Consider the alternative actions in the _Recommended action_ and details that are provided in the following table:

Product or category | Affected item | Version| Replacement | More details and links |
-- | -- | -- | -- | -- |
{{site.data.keyword.mcm_notm}}| web terminal|1.2| Removed | Use the Visual Web Terminal. See the documentation for the common services|
{{site.data.keyword.product}} | Service {{site.data.keyword.catalog}} | version 1.2.0 | Install the service catalog with {{site.data.keyword.open_s}} version 4.1. |  For more information, see _Installing the service catalog_ from the [{{site.data.keyword.ocp_tm}} documentation ![Opens in a new tab](../images/icons/launch-glyph.svg "Opens in a new tab")](https://docs.openshift.com/container-platform/4.1/applications/service_brokers/installing-service-catalog.html){: new_window}.|
Elk| Audit logging|1.2| Removed | You can forward audit logs to your Security information and event management (SIEM) tool. See [Configuring {{site.data.keyword.product}} to forward audit logs](../audit-logging/3.3.0/forward_audit_logs.md)|
Kubernetes audit logs| Audit logging|1.2| Removed | {{site.data.keyword.mcm_notm}} does not collect Kubernetes audit logs.|
APIs - Application management | `deployables.mcm.ibm.com/v1alpha1` |  3.2.1 | `deployable.app.ibm.com/v1alpha1` | [Application resources](../mcm/applications/app_resources.md) |
APIs - Application management | `applicationrelationships.mcm.ibm.com/v1alpha1` | 3.2.1 | `deployable.app.ibm.com.spec.dependencies` | [Application resources](../mcm/applications/app_resources.md) |
{: caption="Table 2. Removed function" caption-side="top"}
