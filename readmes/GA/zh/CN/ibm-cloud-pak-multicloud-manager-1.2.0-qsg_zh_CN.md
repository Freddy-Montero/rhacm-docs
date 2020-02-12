# IBM Cloud Pak for Multicloud Management 1.2 快速入門手冊（包含 Red Hat OpenShift 指引）

<b>產品版本</b>：1.2.0

<b>發佈日期</b>：2019 年 12 月 13 日

<b>前次修改日期</b>：2019 年 12 月 6 日

本手冊提供簡單快速開始使用產品的方法。

## 說明
{: #desc}

IBM Cloud Pak for Multicloud Management 在 Red Hat OpenShift 上執行，提供從內部部署到邊緣的一致可見性、控管及自動化。企業可獲取多叢集管理、事件管理、應用程式管理、基礎架構管理以及現有工具管理等功能。企業可以使用此 IBM Cloud Pak，協助提高由智慧型資料、分析及預測性黃金信號驅動的作業效率，並取得相符性管理的內建支援。

## 目錄
{: #contents}

 1. [線上使用者說明文件](#docs)
 2. [安裝](#install)
 3. [檔案清單](#files)
 4. [IBM Red Hat 安裝手冊](#rhinstall)
 5. [著作權與商標資訊](#notices)

## 線上使用者說明文件
{: #docs}

如需最新的 IBM Cloud Pak for Multicloud Management 使用者說明文件，請參閱 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html。

## 安裝
{: #install}

如需最新的 IBM Cloud Pak for Multicloud Management 安裝說明文件並瞭解如何為安裝做準備，請參閱 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html。

如何瞭解如何使用 IBM 單一登入來配置 Red Hat Ansible Tower，請參閱 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html。

如需瞭解如何使用 IBM 單一登入來配置 Red Hat CloudForms，請參閱 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html。

## 檔案清單
{: #files}

本小節會列出適合於您的組合的檔案（在 IBM Passport Advantage 上提供）。 

表 1. IBM Cloud Pak for Multicloud Management Core 套件
<table border="1" width="100%">
  <tr>
    <th width="50%">說明</th>
    <th width="30%">檔名<br></th>
    <th width="20%">Passport Advantage 產品編號<br></th>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes 映像檔（適用於 AMD64）</td>
    <td>ibm-cp4mcm-core-1.2-x86_64.tar.gz</td>
    <td>CC4L8EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes 映像檔（適用於 Power）</td>
    <td>ibm-cp4mcm-core-1.2-ppc64le.tar.gz</td>
    <td>CC4L9EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 多叢集端點（適用於 AMD64）</td>
    <td>mcm-endpoint-3.3.0-amd64.tgz </td>
    <td>CC4LAEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 多叢集端點（適用於 Power）</td>
    <td>mcm-endpoint-3.3.0-ppc64le.tgz</td>
    <td>CC4LBEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 多叢集端點（適用於 IBM Z）</td>
    <td>mcm-endpoint-3.3.0-s390x.tgz</td>
    <td>CC4LCEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 金鑰管理 HSM</td>
    <td>key-management-hsm-amd64.tar.gz</td>
    <td>CC4PREN</td>
  </tr>
</table>

表 2. IBM Cloud Pak for Multicloud Management 套件的 IBM Red Hat 軟體
<table border="1" width="100%">
  <tr>
    <th width="50%">說明</th>
    <th width="50%">Passport Advantage 產品編號<br></th>
  </tr>
  <tr>
    <td>僅提供英文版 IBM Red Hat Enterprise Linux 7.7</td>
    <td>CC4KJEN</td>
  </tr>
  <tr>
    <td>具有 LSI 邏輯控制器的 Red Hat CloudForms 5 for VMware vSphere</td>
    <td>CC4LEEN</td>
  </tr>
  <tr>
    <td>具有 PVSCSI 控制器的 Red Hat CloudForms 5 for VMware vSphere</td>
    <td>CC4LFEN</td>
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
    <td>Red Hat Ansible Tower 3.6 金鑰</td>
    <td>CC4LGEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management 1.2 的自動化導覽</td>
    <td>CC4MAEN</td>
  </tr>
</table>

表 3. IBM Cloud Pak for Multicloud Management 套件的 IBM Cloud App Management
<table border="1" width="100%">
 <tr>
    <th width="50%">說明</th>
	<th width="30%">檔名<br></th>
    <th width="20%">Passport Advantage 產品編號<br></th>
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

 表 4. IBM Cloud pak for Multicloud Management 套件的 IBM Cloud App Management Extension Pack
<table border="1" width="100%">
 <tr>
    <th width="50%">說明</th>
	<th width="30%">檔名<br></th>
    <th width="20%">Passport Advantage 產品編號<br></th>
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

表格 5. IBM Cloud Automation Manager 套件
<table border="1" width="100%">
  <tr>
    <th width="50%">說明</th>
    <th width="30%">檔名<br></th>
    <th width="20%">Passport Advantage 產品編號<br></th>
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
    <td>IBM Cloud Automation Manager 4.1 for Power Linux LE（64 位元）</td>
    <td>icp-cam-ppc-3.2.2.tar.gz</td>
    <td>CC4E3EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 產品 ID</td>
    <td>icp-cam-prod-id-3.2.2.txt</td>
    <td>CC4E4EN</td>
  </tr>
</table>

## 用於安裝 IBM Cloud Pak for Multicloud Management 1.2 的 Red Hat 軟體的 IBM Red Hat 手冊
{: #rhinstall}

本手冊提供簡單易用的方法來安裝 Red Hat 軟體。

IBM Cloud Pak for Multicloud Management 包含可使用 Red Hat OpenShift Container Platform、Red Hat Enterprise Linux CoreOS (RHCOS) 和 Red Hat Enterprise Linux (RHEL) 的授權。OpenShift Container Platform 主要節點主機只支援 RHCOS 作業系統。OpenShift Container Platform 工作者節點主機同時支援 RHCOS 和 RHEL 作業系統，但 RHCOS 是預設作業系統。

### 安裝 Red Hat OpenShift Container Platform

您可以透過使用 Red Hat 帳戶在以下網址存取 Red Hat OpenShift Cluster Manager 來下載並安裝 OpenShift Container Platform 4.x：https://cloud.redhat.com/openshift/install，該帳戶可以免費建立，無需付費即可獲取對任何 IBM 產品與服務的 Red Hat 訂閱授權。

如果您還沒有 Red Hat 帳戶，請在 https://www.redhat.com/wapps/ugc/register.html 中免費建立一個帳戶，然後再遵循剩下的指示操作。

如果你已有 Red Hat 帳戶，請導覽至 https://cloud.redhat.com/openshift/install 並使用您的帳戶認證來登入。

叢集管理程式會顯示數個圖磚，代表各種雲端提供者和基礎架構類型。請按一下您要在其中安裝 OpenShift Container Platform 的基礎架構類型所對應的圖磚。部分雲端提供者支援安裝程式供應的基礎架構，可在由叢集管理程式自動供應的雲端基礎架構上安裝 OpenShift Container Platform。對於其他雲端提供者和基礎架構類型，可在使用者供應的基礎架構上安裝叢集。

選取您偏好的的基礎架構類型並選擇`安裝程式供應的基礎架構`或`使用者供應的基礎架構`，然後遵循顯示的指示進行操作。

對於任何使用者供應的基礎架構類型（包括「裸機」圖磚），您可以遵循系統向您顯示的一系列簡短步驟進行操作。如需詳細的安裝指示，您可以按一下「入門」鏈結來開啟正式安裝說明文件。對於「裸機」基礎架構類型，請參閱說明文件：https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html。

1. 透過使用叢集管理程式網站提供的鏈結來下載 OpenShift 安裝程式。可透過網際網路直接存取這些檔案，不需要 Red Hat ID 即可下載。
2. 下載或複製您的 OpenShift 取回密碼。此步驟要求您使用 Red Hat ID 登入，但不需要付費訂閱。
3. 透過使用叢集管理程式網站提供的鏈結來下載 Red Hat Enterprise Linux CoreOS (RHCOS)。可透過網際網路直接存取這些檔案，不需要 Red Hat ID 即可下載。
4. 透過使用叢集管理程式網站提供的鏈結來下載 OpenShift 指令行工具 (openshift-install)，並將它們新增至您的 PATH。可透過網際網路直接存取這些檔案，不需要 Red Hat ID 即可下載。
5. 遵循適用於您的基礎架構類型的正式說明文件，透過使用 openshift-install 指令來完成安裝。安裝程式完成之後，您會看到用於存取新叢集的主控台 URL 和認證。系統還會產生 kubeconfig 檔案以搭配您下載的 oc CLI 工具使用。

<img src="red-hat-install.png" alt="說明如何從 IBM Passport Advantage 存取二進位檔以進行手動安裝">

### 選用項目：存取 Red Hat Enterprise Linux 安裝二進位檔

OpenShift Container Platform 主要節點主機只支援 RHCOS 作業系統。OpenShift Container Platform 工作者節點主機同時支援 RHCOS 和 RHEL 作業系統，但 RHCOS 是預設作業系統。如果您偏好使用 Red Hat Enterprise Linux (RHEL) 作為工作者節點主機的作業系統，您需要個別下載 RHEL 安裝二進位檔，因為需要付費訂閱才能下載。

存取及安裝 RHEL 的偏好方法是遵循 Red Hat 中的標準安裝說明文件，並透過使用 Red Hat Network 訂閱來登錄您的系統。可從 Red Hat Customer Portal（網址為 https://access.redhat.com）存取安裝二進位檔、說明文件和授權資訊。如果您是第一次使用 Red Hat 客戶入口網站，請在登入之後按一下*入門*（或使用此鏈結：https://access.redhat.com/start/）以進行引導式導覽，瞭解如何充分利用 Red Hat 訂閱。

### 存取 RHEL 的偏好方法是使用 Red Hat 客戶入口網站

#### 透過 Red Hat 客戶入口網站來存取安裝二進位檔

處理 Cloud Pak 訂單之後，與訂單相關聯的位址將收到一封來自 Red Hat 的電子郵件。此電子郵件列出 Red Hat OpenShift Container Platform 授權數量，並且已更新訂閱。

#### 安裝 Red Hat Enterprise Linux

Red Hat Enterprise Linux 7.6 或更高版本支援 OpenShift Container Platform 4.2。如果已經安裝 Red Hat Enterprise Linux，請使用下列說明文件來完成 Red Hat Enterprise Linux 的安裝。

可透過 Red Hat 客戶入口網站來存取 Red Hat Enterprise Linux 7.7 安裝媒體，網址為https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software

可在 Red Hat 客戶入口網站找到下載及安裝 Red Hat Enterprise Linux 7（包括使用訂閱管理程式來登錄安裝）的指示，網址為 https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

#### 安裝 Red Hat OpenShift Container Platform

順利供應主機或虛擬機器並安裝和登錄 Red Hat Enterprise Linux 之後，請遵循 Red Hat 客戶入口網站（網址為 https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index）中提供的說明文件，繼續安裝 OpenShift Container Platform 4.2

### 存取 RHEL 的替代方法是使用 IBM Passport Advantage

#### 從 IBM Passport Advantage 存取二進位檔以進行手動安裝

如果您需要能夠在 Red Hat 客戶入口網站中更新授權之前安裝 Cloud Pak，則可以使用先前所述的免費 Red Hat ID 來下載安裝 Red Hat OpenShift Container Platform 和 Red Hat Enterprise Linux CoreOS 所必需的所有二進位檔。無法從 IBM Passport Advantage 下載這些二進位檔。

如果選擇安裝 Red Hat Enterprise Linux 作為工作者節點上的主機作業系統，並且您還沒有作用中的 Red Hat 訂閱，則可以透過 IBM Passport Advantage 來存取 Red Hat Enterprise Linux 7.7。可從 IBM Passport Advantage 下載適用於 Red Hat Enterprise Linux 7.7 的安裝映像檔和 RPM（產品編號 CC4KJEN，它是 Cloud Pak eAssembly 的組成部分）。這個檔案在 IBM Passport Advantage 中包含說明 "IBM Red Hat Enterprise Linux English only eImage"。稍後必須登錄此安裝並與 Red Hat Network ID 建立關聯。

下載內容大約為 50 GB，解壓縮檔案需要額外的儲存空間。

此手動安裝程序需要建立本端 HTTP 伺服器來託管所提及下載套件中提供的 RPM 檔案。如果您使用的是偏好的安裝方法，則不需要這些步驟，因為在該情境下您可以透過 Red Hat 網路來存取必要的檔案。

若要執行手動安裝，請遵循下列程序：

1. 從 Passport Advantage 下載 Red Hat Enterprise Linux 安裝檔案（如果您還沒有安裝 Red Hat Enterprise Linux）
2. 供應 Web 伺服器以託管 Yum 儲存庫
3. 將下載的檔案複製到 Web 伺服器
4. 在工作者節點上安裝 Red Hat Enterprise Linux
5. 使用正式說明文件來安裝 OpenShift Container Platform

#### 從 Passport Advantage 下載 Red Hat Enterprise Linux 安裝檔案

登入 IBM Passport Advantage 並下載與 Cloud Pak eAssembly 關聯的 "IBM Red Hat Enterprise Linux English only eImage"（產品編號為 CC4KJEN）。要下載的檔案名稱為 `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`。

#### 供應 Web 伺服器以託管 Yum 儲存庫

使用 HTTP 伺服器來供應實體主機或虛擬機器以支援本端安裝。可使用您選擇的 Web 伺服器作為儲存庫。

如果您還沒有可用的 Web 伺服器，則可以使用 Red Hat 提供的說明文件在 Red Hat Enterprise Linux 上安裝並配置 Apache Web 伺服器，該說明文件位於以下網址中的標題 "Prepare and populate the repository server" 之下：https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server

#### 將下載的檔案複製到 Web 伺服器

將 `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` 複製到 Web 伺服器，並將其解壓縮至 Web 伺服器的文件根目錄下的子目錄 "repos" 中（如果已使用說明文件建立 Web 伺服器，則子目錄為 /var/www/html/repos）。

確保所有使用者都能讀取儲存庫檔案 (chmod -R +r /var/www/html/repos)。

### 在工作者節點上安裝 Red Hat Enterprise Linux

如果尚未安裝 Red Hat Enterprise Linux，請供應主機或虛擬機器以用於 Cloud Pak 安裝所在之 OpenShift Container Platform 叢集的主要節點和工作者節點，並透過使用從 IBM Passport Advantage 下載的 ISO 來安裝 Red Hat Enterprise Linux。

可在 Red Hat 客戶入口網站中找到下載及安裝 Red Hat Enterprise Linux 的完整指示（包括必備項目和主機準備），網址為 https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

* 安裝媒體的 ISO 映像檔 (rhel-server-7.7-x86_64-dvd.iso) 位於您從 IBM Passport Advantage 下載之檔案解壓縮所在的目錄。請使用這些檔案，而不是 Red Hat Enterprise Linux 安裝手冊第 2 章中說明如何從 Red Hat 客戶入口網站下載 Red Hat Enterprise Linux 的步驟。如果是建立虛擬機器來供應節點，則可以直接使用此映像檔。
* 如果是在實體主機上安裝 Red Hat Enterprise Linux，請參閱 Red Hat Enterprise Linux 安裝手冊的第 3 章，以獲取如何建立實體安裝媒體或透過以下網址存取安裝媒體的相關資訊：https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media

#### 使用正式說明文件來安裝 Red Hat OpenShift Container Platform

遵循 Red Hat 提供的說明文件來安裝 OpenShift Container Platform 4.2：https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index


## 著作權與商標資訊
{: #notices}

© Copyright IBM Corporation 2019

U.S. Government Users Restricted Rights - Use, duplication or disclosure restricted by GSA ADP Schedule Contract with IBM Corp.

IBM®、IBM 標誌及 ibm.com® 是 International Business Machines Corp., 在世界許多管轄區註冊的商標。其他產品及服務名稱可能是 IBM 或其他公司的商標。 IBM 商標的最新清單可在 Web 的 "Copyright and trademark information" 中找到，網址為 www.ibm.com/legal/copytrade.shtml。
