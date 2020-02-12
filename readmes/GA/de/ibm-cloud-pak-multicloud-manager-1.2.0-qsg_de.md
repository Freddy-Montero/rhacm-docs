# IBM Cloud Pak for Multicloud Management 1.2 - Leitfaden für den Schnelleinstieg mir Anleitungen für Red Hat OpenShift

<b>Produktrelease</b>: 1.2.0

<b>Veröffentlichungsdatum</b>: 13. Dezember 2019

<b>Datum der letzten Änderung</b>: 6. Dezember 2019

In diesem Leitfaden wird eine schnelle und einfache Methode beschrieben, mit der Sie das Produkt installieren und betriebsbereit machen können. 

## Beschreibung
{: #desc}

IBM Cloud Pak for Multicloud Management, ausgeführt unter Red Hat OpenShift, bietet konsistente Transparenz, Governance und Automatisierung in On-Premises- und Edge-Umgebungen. Unternehmen erhalten die Fähigkeit, Multicluster, Ereignisse, Anwendungen, Infrastrukturen und vorhandene Tools zu verwalten. Sie können dieses IBM Cloud Pak verwenden, um durch intelligente Daten, Analysen und prädiktive golden Signale ihre operative Effizienz zu erhöhen und um die integrierte Unterstützung für das Compliance-Management zu nutzen. 

## Inhalt
{: #contents}

 1. [Onlinebenutzerdokumentation](#docs)
 2. [Installation](#install)
 3. [Liste der Dateien](#files)
 4. [IBM Red Hat-Installationshandbuch](#rhinstall)
 5. [Informationen zu Copyrights und Marken](#notices)

## Onlinebenutzerdokumentation
{: #docs}

Die aktuelle Benutzerdokumentation zu IBM Cloud Pak for Multicloud Management finden Sie unter https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html. 

## Installation
{: #install}

Die aktuelle Installationsdokumentation für IBM Cloud Pak for Multicloud Management und Informationen zum Vorbereiten der Installation finden Sie unter https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html. 

Informationen zum Konfigurieren von Red Hat Ansible Tower mit IBM Single Sign-on finden Sie unter https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html. 

Informationen zum Konfigurieren von Red Hat CloudForms mit IBM Single Sign-on finden Sie unter https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html. 

## Liste der Dateien
{: #files}

In diesem Abschnitt werden die Dateien aufgelistet, die in IBM Passport Advantage für Ihr Bundle verfügbar sind. 

Tabelle 1. Basispakete für IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
  <tr>
    <th width="50%">Beschreibung</th>
    <th width="30%">Dateiname<br></th>
    <th width="20%">Teilenummer bei Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes image for AMD64</td>
    <td>ibm-cp4mcm-core-1.2-x86_64.tar.gz</td>
    <td>CC4L8EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes image for Power</td>
    <td>ibm-cp4mcm-core-1.2-ppc64le.tar.gz</td>
    <td>CC4L9EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint for AMD64</td>
    <td>mcm-endpoint-3.3.0-amd64.tgz </td>
    <td>CC4LAEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint for Power</td>
    <td>mcm-endpoint-3.3.0-ppc64le.tgz</td>
    <td>CC4LBEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint for IBM Z</td>
    <td>mcm-endpoint-3.3.0-s390x.tgz</td>
    <td>CC4LCEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Key Management HSM</td>
    <td>key-management-hsm-amd64.tar.gz</td>
    <td>CC4PREN</td>
  </tr>
</table>

Tabelle 2. Pakete für IBM Red Hat-Software für IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
  <tr>
    <th width="50%">Beschreibung</th>
    <th width="50%">Teilenummer bei Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Red Hat Enterprise Linux 7.7 English Only</td>
    <td>CC4KJEN</td>
  </tr>
  <tr>
    <td>Red Hat CloudForms 5 for VMware vSphere with LSI Logic controller</td>
    <td>CC4LEEN</td>
  </tr>
  <tr>
    <td>Red Hat CloudForms 5 for VMware vSphere with PVSCSI controller</td>
    <td>CC4LFEN </td>
  </tr>
  <tr>
    <td>Red Hat CloudForms 5 for Red Hat OpenStack Platform</td>
    <td>CC4PSEN</td>
  </tr>
  <tr>
    <td>Red Hat CloudForms 5 for Red Hat Virtualization</td>
    <td>CC4PTEN</td>
  </tr>
  <tr>
    <td>Red Hat CloudForms 5 for Microsoft SCVMM</td>
    <td>CC4PUEN</td>
  </tr>
  <tr>
    <td>Red Hat Ansible Tower 3.6 key</td>
    <td>CC4LGEN</td>
  </tr>
  <tr>
    <td>Automation navigation for IBM Cloud Pak for Multicloud Management 1.2</td>
    <td>CC4MAEN</td>
  </tr>
</table>

Tabelle 3. Pakete für IBM Cloud App Management für IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Beschreibung</th>
	<th width="30%">Dateiname<br></th>
    <th width="20%">Teilenummer bei Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Server Install </td>
	<td>icam_ppa_2019.4.0_prod.tar.gz</td>
    <td>CC4KNEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Server Install on Power for ICPMM 1.2</td>
	<td>icam_ppa_2019.4.0_prod_ppc64le.tar.gz</td>
    <td>CC4LHEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install xLinux </td>
	<td>appMgtAgents_xlinux_2019.4.0.tar.gz</td>
    <td>CC4KPEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install Windows </td>
	<td>appMgtAgents_win_2019.4.0.zip </td>
    <td>CC4KQEN</td>
  </tr>
    <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install AIX</td>
	<td>appMgtAgents_aix_2019.4.0.tar.gz </td>
    <td>CC4KREN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Data Collectors Install </td>
	<td>appMgtDataCollectors_2019.4.0.tar.gz</td>
    <td>CC4KSEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install zLinux </td>
	<td>appMgtAgents_zlinux_2019.4.0.tar.gz</td>
    <td>CC4KTEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install Solaris Sparc</td>
	<td>appMgtAgents_solaris_2019.4.0.tar.gz</td>
    <td>CC4KUEN</td>
  </tr>
    <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install PLinux</td>
	<td>appMgtAgents_plinux_2019.4.0.tar.gz</td>
    <td>CC4KVEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Agents Install PLinuxLE</td>
	<td>appMgtAgents_plinuxle_2019.4.0.tar.gz</td>
    <td>CC4KWEN</td>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 for Eventing Klusterlet Config</td>
	<td>agent_ppa_2019.4.0_prod.tar.gz</td>
    <td>CC4KXEN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 for Eventing Server Side</td>
	<td>icam_ppa_2019.4.0_prod_lite.tar.gz</td>
    <td>CC4KYEN</td>
  </tr>
   <tr>
    <td>IBM Cloud App Management V2019.4.0 for Eventing Klusterlet Config on AMD64</td>
	<td>agent_ppa_2019.4.0_prod_amd64.tar.gz</td>
    <td>CC4KZEN</td>
  </tr>
   <tr>
    <td>IBM Cloud App Management V2019.4.0 for Eventing Server Side on AMD64</td>
	<td>icam_ppa_2019.4.0_prod_lite_amd64.tar.gz</td>
    <td>CC4L0EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Unified Agent V2019.4.0</td>
	<td>unifiedAgent_2019.4.0.tar.gz</td>
    <td>CC4L1EN</td>
  </tr>
  <tr>
    <td> IBM Cloud App Management V2019.4.0 Agents Install Solaris X86 </td>
    <td>appMgtAgents_solaris_x86_2019.4.0.tar.gz</td>
    <td>CC4L2EN</td>
  </tr>
  </table>

 Tabelle 4. Pakete für IBM Cloud App Management Extension Pack für IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Beschreibung</th>
	<th width="30%">Dateiname<br></th>
    <th width="20%">Teilenummer bei Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Extension Pack xLinux</td>
	<td>appMgtExt_xlinux_2019.4.0.tar</td>
    <td>CC4L3EN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Extension Pack Windows</td>
	<td>appMgtExt_win_2019.4.0.zip </td>
    <td>CC4L4EN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Extension Pack AIX</td>
	<td>appMgtExt_aix_2019.4.0.tar</td>
    <td>CC4L5EN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Extension Pack PLinux</td>
	<td>appMgtExt_plinux_2019.4.0.tar</td>
    <td>CC4L6EN</td>
  </tr>
  <tr>
    <td>IBM Cloud App Management V2019.4.0 Extension Pack PLinuxLE</td>
	<td>appMgtExt_plinuxle_2019.4.0.tar</td>
    <td>CC4L7EN</td>
  </tr>
</table>

Tabelle 5. Pakete für IBM Cloud Automation Manager
<table border="1" width="100%">
  <tr>
    <th width="50%">Beschreibung</th>
    <th width="30%">Dateiname<br></th>
    <th width="20%">Teilenummer bei Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 for Linux (x86_64)</td>
    <td>icp-cam-x86_64-3.2.2.tar.gz</td>
    <td>CC4E1EN</td>
  </tr>
  <tr>
  <td>IBM Cloud Automation Manager 4.1 for IBM Z</td>
    <td>icp-cam-s390x-3.2.2.tar.gz</td>
    <td>CC4E2EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 for Power Linux LE (64-bit)</td>
    <td>icp-cam-ppc-3.2.2.tar.gz</td>
    <td>CC4E3EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 Product ID</td>
    <td>icp-cam-prod-id-3.2.2.txt</td>
    <td>CC4E4EN</td>
  </tr>
</table>

## IBM Red Hat - Leitfaden für die Installation von Red Hat-Software für IBM Cloud Pak for Multicloud Management 1.2
{: #rhinstall}

In diesem Leitfaden wird eine schnelle und einfache Methode zur Installation von Red Hat-Software beschrieben. 

IBM Cloud Pak for Multicloud Management umfasst die Berechtigung zur Verwendung von Red Hat OpenShift Container Platform, Red Hat Enterprise Linux CoreOS (RHCOS) und Red Hat Enterprise Linux (RHEL). Für OpenShift Container Platform-Masterknoten-Hosts ist RHCOS das einzige unterstützte Betriebssystem. Für OpenShift Container Platform-Workerknoten-Hosts werden die Betriebssysteme RHCOS und RHEL unterstützt, wobei RHCOS das Standardbetriebssystem ist. 

### Red Hat OpenShift Container Platform installieren

OpenShift Container Platform 4.x kann mithilfe von Red Hat OpenShift Cluster Manager unter der Adresse https://cloud.redhat.com/openshift/install heruntergeladen und installiert werden. Für diese Aktionen müssen Sie Ihr Red Hat-Konto verwenden, das kostenlos erstellt werden kann, ohne dass ein gebührenpflichtiges Red Hat-Subskriptionsrecht für ein IBM Angebot erforderlich ist. 

Wenn Sie noch nicht über ein Red Hat-Konto verfügen, können Sie es unter https://www.redhat.com/wapps/ugc/register.html kostenlos erstellen, bevor Sie die weiteren Anweisungen befolgen. 

Wenn Sie über ein Red Hat-Konto verfügen, öffnen Sie die Seite https://cloud.redhat.com/openshift/install und melden Sie sich mit Ihren Kontoberechtigungsnachweisen an. 

Im Cluster-Manager werden mehrere Titel angezeigt, die verschiedene Cloud-Provider und Infrastrukturtypen angeben. Klicken Sie auf die Kachel für den Typ der Infrastruktur, in der Sie OpenShift Container Platform installieren wollen. Bestimmte Cloud-Provider unterstützen die vom Installationsprogramm bereitgestellte Infrastruktur (Installer-Provisioned Infrastructure). Bei diesem Verfahren wird OpenShift Container Platform in einer Cloud-Infrastruktur installiert, die automatisch vom Cluster-Manager bereitgestellt wird. Bei anderen Cloud-Providern oder Infrastrukturtypen kann ein Cluster in einer vom Benutzer bereitgestellten Infrastruktur (User-Provisioned Infrastructure) installiert werden. 

Wählen Sie Ihren bevorzugten Infrastrukturtyp aus und wählen Sie anschließend `Installer-Provisioned Infrastructure` oder `User-Provisioned Infrastructure` aus und befolgen Sie die angezeigten Anweisungen. 

Bei den vom Benutzer bereitgestellten Infrastrukturtypen (einschließlich der Kachel für “Bare Metal”) wird eine kurze Serie von Schritten angezeigt, die Sie befolgen müssen. Detaillierte Installationsanweisungen erhalten Sie, wenn Sie auf den Link “Get Started” klicken, um die offizielle Installationsdokumentation zu öffnen. Für den Infrastrukturtyp “Bare Metal” finden Sie weitere Informationen in der folgenden Dokumentation: https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html. 

1. Laden Sie das OpenShift-Installationsprogramm herunter. Verwenden Sie dazu den auf der Website des Cluster-Managers angegebenen Link. Auf diese Dateien kann direkt über das Internet zugegriffen werden; zum Herunterladen ist keine Red Hat-ID erforderlich. 
2. Laden Sie den geheimen Schlüssel für Pull-Operationen für OpenShift herunter oder kopieren Sie ihn. Für diesen Schritt müssen Sie mit einer Red Hat-ID angemeldet sein, es ist jedoch keine gebührenpflichtige Subskription erforderlich. 
3. Laden Sie Red Hat Enterprise Linux CoreOS (RHCOS)  herunter. Verwenden Sie dazu den auf der Website des Cluster-Managers angegebenen Link. Auf diese Dateien kann direkt über das Internet zugegriffen werden; zum Herunterladen ist keine Red Hat-ID erforderlich. 
4. Laden Sie die OpenShift-Befehlszeilentools (openshift-install) herunter und fügen Sie sie zur Angabe PATH hinzu. Verwenden Sie zum Herunterladen den auf der Website des Cluster-Managers angegebenen Link. Auf diese Dateien kann direkt über das Internet zugegriffen werden; zum Herunterladen ist keine Red Hat-ID erforderlich. 
5. Befolgen Sie die Informationen in der offiziellen Dokumentation für Ihren Infrastrukturtyp und führen Sie die Installation mit dem Befehl 'openshift-install' aus. Nach Abschluss des Installationsprogramms werden die Konsolen-URL und die Berechtigungen für den Zugriff auf den neuen Cluster angezeigt. Darüber hinaus wird automatisch eine 'kubeconfig'-Datei generiert, die Sie mit den heruntergeladenen CLI-Tools verwenden können. 

<img src="red-hat-install.png" alt="Beschreibt den Zugriff auf die Binärdateien für die manuelle Installation über IBM Passport Advantage">

### Optional: Auf die Binärdateien für die Installation von Red Hat Enterprise Linux zugreifen

Für OpenShift Container Platform-Masterknoten-Hosts ist RHCOS das einzige unterstützte Betriebssystem. Für OpenShift Container Platform-Workerknoten-Hosts werden die Betriebssysteme RHCOS und RHEL unterstützt, wobei RHCOS das Standardbetriebssystem ist. Wenn Sie bevorzugen, Red Hat Enterprise Linux (RHEL) als Betriebssystem für die Workerknoten-Hosts zu verwenden, müssen Sie die Binärdateien für die RHEL-Installation separat herunterladen, da sie nur mit einer gebührenpflichtigen Berechtigung verfügbar sind. 

Das bevorzugte Verfahren für den Zugriff auf und die Installation von RHEL besteht darin, die Standardinstallationsdokumentation von Red Hat zu befolgen und Ihre Systeme mithilfe Ihrer Red Hat Network-Subskription zu registrieren. Auf die Binärdateien für die Installation, die Dokumentation und die Berechtigungsinformationen kann über das Red Hat-Kundenportal unter der Adresse https://access.redhat.com zugegriffen werden. Wenn Sie das Red Hat-Kundenportal zuvor noch nicht genutzt haben, können Sie nach der Anmeldung auf *Getting Started* klicken (oder den Link https://access.redhat.com/start/ verwenden) um eine geführte Tour zu unternehmen und zu erfahren, wie Sie Ihre Red Hat-Subskription optimal nutzen. 

### Bevorzugte Methode für den Zugriff auf RHEL: Verwendung des Red Hat-Kundenportals

#### Über das Red Hat-Kundenportal auf die Binärdateien für die Installation zugreifen

Nachdem Ihre Cloud-Pak-Bestellung verarbeitet wurde, erhalten Sie unter der Adresse, die Ihrer Bestellung zugeordnet ist, eine E-Mail von Red Hat. Diese E-Mail enthält die Anzahl der Berechtigungen für Red Hat OpenShift Container Platform sowie die Information, dass die Subskription aktualisiert wurde. 

#### Red Hat Enterprise Linux installieren

OpenShift Container Platform 4.2 wird unter Red Hat Enterprise Linux ab Version 7.6 unterstützt. Wenn Sie Red Hat Enterprise Linux noch nicht installiert haben, können Sie die nachfolgende Dokumentation verwenden, um die Installation von Red Hat Enterprise Linux auszuführen. 

Auf die Installationsmedien für Hat Enterprise Linux 7.7 kann über das Red Hat-Kundenportal unter der Adresse https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software zugegriffen werden. 

Anweisungen zum Herunterladen und Installieren von Red Hat Enterprise Linux 7, einschließlich der Registrierung Ihrer Installation mithilfe des Subskriptionsmanagers, finden Sie im Red Hat-Kundenportal unter der Adresse https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started. 

#### Red Hat OpenShift Container Platform installieren

Nachdem Sie Hosts oder virtuellen Maschinen erfolgreich mit installiertem Red Hat Enterprise Linux bereitgestellt haben, können Sie im nächsten Schritt OpenShift Container Platform 4.2 installieren. Befolgen Sie dazu die im Red Hat-Kundenportal unter https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index bereitgestellt Dokumentation. 

### Alternative Methode für den Zugriff auf RHEL: Verwendung von IBM Passport Advantage

#### Über Passport Advantage auf die Binärdateien für die manuelle Installation zugreifen

Wenn Sie in der Lage sein wollen, das Cloud Pak zu installieren, bevor die Berechtigungen im Red Hat-Kundenportal aktualisiert wurden, können Sie alle Binärdateien, die zur Installation von Red Hat OpenShift Container Platform und Red Hat Enterprise Linux CoreOS erforderlich sind, mit einer kostenlos erhältlichen Red Hat-ID herunterladen. Dieses Verfahren ist weiter oben beschrieben. Diese Binärdateien sind nicht zum Download über IBM Passport Advantage verfügbar. 

Wenn Sie zuerst Red Hat Enterprise Linux als Hostbetriebssystem auf den Workerknoten installieren wollen und Sie noch nicht über eine aktive Red Hat-Subskription verfügen, können Sie über IBM Passport Advantage auf Red Hat Enterprise Linux 7.7 zugreifen. Die Installationsimages und RPMs für Red Hat Enterprise Linux 7.7 können von IBM Passport Advantage heruntergeladen werden (Teilenummer CC4KJEN); sie sind Teil Ihrer Cloud-Pak-E-Assembly. Diese Datei hat in IBM Passport Advantage die Beschreibung “IBM Red Hat Enterprise Linux English only eImage”. Diese Installation muss später registriert und Ihrer Red Hat Network-ID zugeordnet werden. 

Der Download ist etwa 50 GB groß. Zum Extrahieren der Dateien ist zusätzlicher Speicherplatz erforderlich. 

Für diesen manuellen Installationsprozess muss ein lokaler HTTP-Server erstellt werden, auf dem die RPM-Dateien gehostet werden, die in dem genannten Downloadpaket bereitgestellt werden. Diese Schritte sind nicht erforderlich, wenn Sie die bevorzugte Installationsmethode verwenden, da der Zugriff auf die erforderlichen Dateien bei diesem Szenario über das Red Hat Network ermöglicht wird. 

Gehen Sie wie folgt vor, um eine manuelle Installation durchzuführen: 

1. Installationsdateien für Red Hat Enterprise Linux von Passport Advantage herunterladen (sofern Red Hat Enterprise Linux noch nicht installiert ist) 
2. Web-Server zum Hosten eines Yum-Repositorys bereitstellen 
3. Heruntergeladene Dateien auf den Web-Server kopieren 
4. Red Hat Enterprise Linux auf den Workerknoten installieren 
5. OpenShift Container Platform mithilfe der Informationen in der offiziellen Dokumentation installieren 

#### Installationsdateien für Red Hat Enterprise Linux von Passport Advantage herunterladen 

Melden Sie sich bei IBM Passport Advantage an und laden Sie die Datei mit der Beschreibung “IBM Red Hat Enterprise Linux English only eImage” (Teilenummer CC4KJEN) herunter. Die Datei ist der Cloud Pak-E-Assembly zugeordnet. Der Name der herunterzuladenden Datei ist `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`. 

#### Web-Server zum Hosten eines Yum-Repositorys bereitstellen 

Stellen Sie dem physischen Host oder der virtuellen Maschine einen HTTP-Server bereit, um die lokale Installation zu unterstützen. Sie können einen Web-Server Ihrer Wahl als Repository verwenden. 

Wenn Ihnen keinen Web-Server zur Verfügung steht, können Sie den Apache-Web-Server auf einem Red Hat Enterprise Linux-System installieren und konfigurieren. Verwenden Sie dazu die Informationen im Abschnitt “Prepare and populate the repository server” unter https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server in der von Red Hat bereitgestellten Dokumentation. 

#### Heruntergeladene Dateien auf den Web-Server kopieren 

Kopieren Sie `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` auf den Web-Server und extrahieren Sie die Datei in ein Unterverzeichnis mit dem Namen “repos” unterhalb des Dokumentstammverzeichnisses des Web-Servers (/var/www/html/repos, wenn Sie den Web-Server anhand der Dokumentation erstellt haben). 

Stellen Sie sicher, dass die Repository-Dateien von allen Benutzern gelesen werden können (chmod -R +r /var/www/html/repos). 

### Red Hat Enterprise Linux auf den Workerknoten installieren 

Wenn Red Hat Enterprise Linux noch nicht installiert ist, müssen Sie die Hosts oder VMs bereitstellen, die für die Master- oder Workerknoten für den OpenShift Container Platform-Cluster verwendet werden, auf dem das Cloud-Pak installiert wird, und dann Red Hat Enterprise Linux mit dem von IBM Passport Advantage heruntergeladenen ISO-Image installieren. 

Die vollständigen Anweisungen zum Herunterladen und Installieren von Red Hat Enterprise Linux, einschließlich der Informationen zu Voraussetzungen und zur Vorbereitung des Hosts, finden Sie im Red Hat-Kundenportal unter der Adresse https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started. 

* Ein ISO-Image des Installationsmediums (rhel-server-7.7-x86_64-dvd.iso) befindet sich in dem Verzeichnis, in das Sie die von IBM Passport Advantage heruntergeladene Datei extrahiert haben. Verwenden Sie diese Dateien anstelle der in Kapitel 2 des Installationshandbuchs für Red Hat Enterprise Linux angegebenen Schritte, in denen das Herunterladen von Red Hat Enterprise Linux aus dem Red Hat-Kundenportal beschrieben wird. Wenn Sie virtuelle Maschinen verwenden, um die Knoten bereitzustellen, kann dieses Image direkt verwendet werden. 
* Wenn Sie Red Hat Enterprise Linux auf einem physischen Host installieren, finden Sie weitere Informationen zum Erstellen der physischen Installationsmedien oder zum Zugreifen auf die Installationsmedien über ein Netz in Kapitel 3 des Installationshandbuchs für Red Hat Enterprise Linux unter der folgenden Adresse: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media. 

#### Red Hat OpenShift Container Platform mithilfe der offiziellen Dokumentation installieren 

Befolgen Sie die von Red Hat bereitgestellte Dokumentation und installieren Sie OpenShift Container Platform 4.2. Informationen hierzu finden Sie unter https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index. 


## Informationen zu Copyrights und Marken
{: #notices}

© Copyright IBM Corporation 2019

U.S. Government Users Restricted Rights - Use, duplication or disclosure restricted by GSA ADP Schedule Contract with IBM Corp.

IBM®, das IBM Logo und ibm.com sind eingetragene Marken der IBM Corporation in den USA und/oder anderen Ländern. Weitere Produkt- und Servicenamen können Marken von IBM oder anderen Unternehmen sein. Eine aktuelle Liste der IBM Marken finden Sie auf der Webseite "Copyright and trademark information" unter www.ibm.com/legal/copytrade.shtml.
