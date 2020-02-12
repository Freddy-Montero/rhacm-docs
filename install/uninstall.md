---

copyright:
  years: 2019
lastupdated: "2019-12-12"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:child: .link .ulchildlink}
{:childlinks: .ullinks}

# Uninstalling the {{site.data.keyword.cloud_pak_mcm}} offline

Uninstall {{site.data.keyword.cloud_pak_mcm}} by removing all deployed platform Helm charts.
{:shortdesc}

1. If applicable, uninstall any optional modules. For details, see the following topics:
   - [Uninstalling IBM Cloud App Management](https://www.ibm.com/support/knowledgecenter/SS8G7U_19.4.0/com.ibm.app.mgmt.doc/content/uninstall_mcm_icam_intro.html?cp=SSFC4F_1.2.0)
   - [Uninstalling IBM Cloud Automation Manager](https://www.ibm.com/support/knowledgecenter/SS2L37_4.1.0.0/cam_uninstalling.html?cp=SSFC4F_1.2.0)
2. Log in to the boot node as a user with root permissions. During installation, you specified the IP addresses for each node type.
3. Change to the `cluster` directory within your {{site.data.keyword.cloud_pak_mcm}} installation directory:
    ```
    cd /<installation_directory>/cluster
    ```
    {: codeblock}

4. Uninstall {{site.data.keyword.cloud_pak_mcm}} by running the `uninstall-with-openshift` command:
    ```
    sudo docker run -t --net=host -e LICENSE=accept -v $(pwd):/installer/cluster:z -v /var/run:/var/run:z -v /etc/docker:/etc/docker:z --security-opt label:disable ibmcom/mcm-inception-amd64:3.2.3-rhel-ee uninstall-with-openshift
    ```
    {: codeblock}

**Note:** If `multicluster-hub.etcd.persistence` is set to `true` in the `config.yaml` file, the persistence volume for etcd is retained after you uninstall. The `config.yaml` file is located in the `/<installation_directory>/cluster` folder. You must back up the data of the persistence volume and then delete the persistence volume manually.
