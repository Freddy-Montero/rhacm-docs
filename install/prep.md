---

copyright:
  years: 2020
lastupdated: "2020-03-31"

---

# Preparing to install Red Hat Advanced Cluster Management for Kubernetes

Before you install Red Hat Advanced Cluster Management for Kubernetes, review the following installation requirements.

## Red Hat OpenShift Container Platform

* You must have a supported Red Hat OpenShift Container Platform version, including the registry and storage services, installed and working in your cluster. For more information about installing the Red Hat OpenShift Container Platform, see the Red Hat OpenShift documentation. 

  * For Red Hat OpenShift Container Platform version 4.3, see [Red Hat OpenShift Container Platform 4.3 Documentation](https://docs.openshift.com/container-platform/4.3/welcome/index.html).
  * For Red Hat OpenShift Container Platform version 4.2, see [Red Hat OpenShift Container Platform 4.2 Documentation](https://docs.openshift.com/container-platform/4.2/welcome/index.html).
  
* To ensure that the Red Hat OpenShift Container Platform cluster is set up correctly, access the Red Hat OpenShift Container Platform web console.

  Run the `kubectl -n openshift-console get route` command to access the Red Hat OpenShift Container Platform web console. See the following example output:
  
    ```
    openshift-console          console             console-openshift-console.apps.new-coral.purple-chesterfield.com                       console                  https   reencrypt/Redirect     None
    ```

	The console URL in this example is `https:// console-openshift-console.apps.new-coral.purple-chesterfield.com`. Open the URL in your browser and check the result. If the console URL displays `console-openshift-console.router.default.svc.cluster.local`, set `openshift_master_default_subdomain` when you install the Red Hat OpenShift Container Platform. 



