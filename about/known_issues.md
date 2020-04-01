---

copyright:
  years: 2020
lastupdated: "2020-03-25"

---

# Known issues

Review the known issues for Red Hat Advanced Cluster Management for Kubernetes. 

  - [Certificate manager must not exist during an installation](#678)
  - [LDAP user names are case-sensitive](#25735)
  - [CIS policy controller is not installed](#1087)
  - [Console might not display in Firefox earlier versions](#1100)

## Certificate manager must not exist during an installation
{: #678}

Certificate manager must not exist on a cluster when you install Red Hat Advanced Cluster Management for Kubernetes.

When certificate manager already exists on the cluster, Red Hat Advanced Cluster Management for Kubernetes installation fails. 

To resolve this issue, verify if the certificate manager is present in your cluster by running the following command: 

   ```
   kubectl get crd | grep certificates.certmanager
   ```

## LDAP user names are case-sensitive
{: #25735}

LDAP user names are case-sensitive. You must use the name exactly the way it is configured in your LDAP directory.

## CIS policy controller is not installed
{: #1087}

The CIS policy controller is disabled by default when you install Red Hat Advanced Cluster Management for Kubernetes, If you create a CIS policy, you might receive the following message:

   ```
   CIS policy controller is not installed
   ```

You must enable the CIS policy controller. For more information, see _Enable the CIS controller_ on the [CIS policy controller page](../governance/cis_policy_ctrl.md#cisc).

## Some console features might not display in Firefox earlier versions
{: #1100}

The product supports Mozilla Firefox 74.0 or the latest version that is available for Linux, macOS, and Windows. Upgrade to the latest version for the best console compatibility.

## CRD for a managed cluster must be ready before importing
{: #1311}

If you receive the following error when you import a cluster, the required CRD might not be ready:

  ```
  error: unable to recognize "STDIN": no matches for kind "Endpoint" in version "multicloud.ibm.com/v1beta1"
  ```

  To resolve, import the cluster again.


