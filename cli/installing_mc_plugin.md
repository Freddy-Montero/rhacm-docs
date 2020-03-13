---

copyright:
  years: 2020
lastupdated: "2020-03-09"

---

# Installing the multicluster plug-in (mc)

The `mc` plug-in is installed after you install the OpenShift Container Platform command-line interface (CLI) tool. You can use the multicluster plug-in (mc) to view information about your clusters, manage your clusters, deploy applications, and more.
{:shortdesc}

## Prerequisites

* You must install the CLI [installation documentation](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.3/html/cli_tools/openshift-cli-oc) to install the OpenShift Container Platform command-line interface (CLI).

## Installing the plug-in

1. Download the multicluster, or `mc` plug-in for the applicable operating system. See the list of the `mc` plug-in commands for the different operating systems:

  For macOS, run the following command: < list of os and commands needed >
   
2. Install the `mc` plugin for `oc`. Run the following command to install the plug-in:

  ```
  oc plugin install -f oc-mc-plugin
  ```
  {: codeblock}

3. Verify that the `mc` plugin for `oc` was successfully installed. Run the following command:

  ```
  oc mc -help
  ```
  {: codeblock}

  See the following output:

  ```
  NAME:
     oc mc

  USAGE:
     oc mc command [arguments...] [command options]

  COMMANDS:
     apply                Apply a configuration to a resource by `filename` or `stdin`.
     cluster create       Create a cluster resource for import
     cluster delete       Delete a cluster. This will remove the cluster from management and delete management components from the cluster if connected.
     cluster import       Output the YAML content to be applied to the cluster to import it.
     cluster template     Output a template config.yaml file used for cluster import
     cluster update       Update a cluster resource for import
     create               Create a resource from a file or from stdin
     create helmrepo      Create a Helm repository
     delete               Delete resources by file names, stdin, resources and names, or by resources and label selector
     deploy application   Deploy an application
     describe             Show details of a specific resource or group of resources
     edit                 Edit a resource from the default editor
     get                  Display one or many resources
     label                Update the labels on a resource
     logs, log            Print the logs for a container in a pod
     help
  ```
  {: pre}

  Enter `oc mc help [command]` for more information about a command.
