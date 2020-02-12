# IBM Cloud Pak for Multicloud Management 1.2 빠른 시작 안내서(Red Hat OpenShift 안내 포함)

<b>제품 릴리스</b>: 1.2.0

<b>공개 날짜</b>: 2019년 12월 13일

<b>마지막 수정 날짜</b>: 2019년 12월 6일

이 안내서는 제품을 빠르고 쉽게 실행할 수 있는 방법을 제공합니다.

## 설명
{: #desc}

Red Hat OpenShift에서 실행되는 IBM Cloud Pak for Multicloud Management는 온프레미스에서 에지로의 일관된 가시성, 통제 및 자동화를 제공합니다. 엔터프라이즈는 멀티클러스터 관리, 이벤트 관리, 애플리케이션 관리, 인프라 관리, 기존 도구 관리 등의 기능을 얻습니다. 엔터프라이즈는 이 IBM Cloud Pak을 사용하여 지능형 데이터, 분석 및 예측적 골드 신호로 구동되는 운영 효율성을 높이고 규제 준수 관리에 대한 기본 제공 지원을 받을 수 있습니다.

## 목차
{: #contents}

 1. [온라인 사용자 문서](#docs)
 2. [설치](#install)
 3. [파일 목록](#files)
 4. [IBM Red Hat 설치 안내서](#rhinstall)
 5. [저작권 및 상표 정보](#notices)

## 온라인 사용자 문서
{: #docs}

최신 IBM Cloud Pak for Multicloud Management 사용자 문서는 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html 페이지를 참조하십시오. 

## 설치
{: #install}

최신 IBM Cloud Pak for Multicloud Management 설치 문서 및 설치 준비 방법은 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html 페이지를 참조하십시오. 

IBM 싱글 사인온으로 Red Hat Ansible Tower를 구성하는 데 대한 정보는 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html 페이지를 참조하십시오. 

IBM 싱글 사인온으로 Red Hat CloudForms를 구성하는 데 대한 정보는 https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html 페이지를 참조하십시오. 

## 파일 목록
{: #files}

이 섹션은 사용자 번들에 대해 IBM Passport Advantage에서 사용 가능한 파일을 나열합니다.

표 1. IBM Cloud Pak for Multicloud Management 코어 패키지
<table border="1" width="100%">
  <tr>
    <th width="50%">설명</th>
    <th width="30%">파일 이름<br></th>
    <th width="20%">Passport Advantage 부품 번호<br></th>
  </tr>
  <tr>
    <td>AMD64용 IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes 이미지</td>
    <td>ibm-cp4mcm-core-1.2-x86_64.tar.gz</td>
    <td>CC4L8EN</td>
  </tr>
  <tr>
    <td>Power용 IBM Cloud Pak for Multicloud Management Core 1.2 Kubernetes 이미지</td>
    <td>ibm-cp4mcm-core-1.2-ppc64le.tar.gz</td>
    <td>CC4L9EN</td>
  </tr>
  <tr>
    <td>AMD64용 IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint</td>
    <td>mcm-endpoint-3.3.0-amd64.tgz</td>
    <td>CC4LAEN</td>
  </tr>
  <tr>
    <td>Power용 IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint</td>
    <td>mcm-endpoint-3.3.0-ppc64le.tgz</td>
    <td>CC4LBEN</td>
  </tr>
  <tr>
    <td>IBM Z용 IBM Cloud Pak for Multicloud Management Core 1.2 Multicluster-endpoint</td>
    <td>mcm-endpoint-3.3.0-s390x.tgz</td>
    <td>CC4LCEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management Core 1.2 키 관리 HSM</td>
    <td>key-management-hsm-amd64.tar.gz</td>
    <td>CC4PREN</td>
  </tr>
</table>

표 2. IBM Cloud Pak for Multicloud Management 패키지용 IBM Red Hat 소프트웨어
<table border="1" width="100%">
  <tr>
    <th width="50%">설명</th>
    <th width="50%">Passport Advantage 부품 번호<br></th>
  </tr>
  <tr>
    <td>IBM Red Hat Enterprise Linux 7.7(영어 전용)</td>
    <td>CC4KJEN</td>
  </tr>
  <tr>
    <td>VMware vSphere(LSI Logic 제어기 사용)용 Red Hat CloudForms 5</td>
    <td>CC4LEEN</td>
  </tr>
  <tr>
    <td>VMware vSphere(PVSCSI 제어기 사용)용 Red Hat CloudForms 5</td>
    <td>CC4LFEN</td>
  </tr>
  <tr>
    <td>Red Hat OpenStack Platform용 Red Hat CloudForms 5</td>
    <td>CC4PSEN</td>
  </tr>
  <tr>
    <td>Red Hat Virtualization용 Red Hat CloudForms 5</td>
    <td>CC4PTEN</td>
  </tr>
  <tr>
    <td>Microsoft SCVMM용 Red Hat CloudForms 5</td>
    <td>CC4PUEN</td>
  </tr>
  <tr>
    <td>Red Hat Ansible Tower 3.6 키</td>
    <td>CC4LGEN</td>
  </tr>
  <tr>
    <td>IBM Cloud Pak for Multicloud Management 1.2용 자동화 탐색</td>
    <td>CC4MAEN</td>
  </tr>
</table>

표 3. IBM Cloud Pak for Multicloud Management 패키지용 IBM Cloud App Management
<table border="1" width="100%">
  <tr>
    <th width="50%">설명</th>
	<th width="30%">파일 이름<br></th>
    <th width="20%">Passport Advantage 부품 번호<br></th>
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

 표 4. IBM Cloud Pak for Multicloud Management 패키지용 IBM Cloud App Management 확장 팩
<table border="1" width="100%">
  <tr>
    <th width="50%">설명</th>
	<th width="30%">파일 이름<br></th>
    <th width="20%">Passport Advantage 부품 번호<br></th>
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

표 5. IBM Cloud Automation Manager 패키지
<table border="1" width="100%">
  <tr>
    <th width="50%">설명</th>
    <th width="30%">파일 이름<br></th>
    <th width="20%">Passport Advantage 부품 번호<br></th>
  </tr>
  <tr>
    <td>Linux(x86_64)용 IBM Cloud Automation Manager 4.1</td>
    <td>icp-cam-x86_64-3.2.2.tar.gz</td>
    <td>CC4E1EN</td>
  </tr>
  <tr>
  <td>IBM Z용 IBM Cloud Automation Manager 4.1</td>
    <td>icp-cam-s390x-3.2.2.tar.gz</td>
    <td>CC4E2EN</td>
  </tr>
  <tr>
    <td>Power Linux LE(64비트)용 IBM Cloud Automation Manager 4.1</td>
    <td>icp-cam-ppc-3.2.2.tar.gz</td>
    <td>CC4E3EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 제품 ID</td>
    <td>icp-cam-prod-id-3.2.2.txt</td>
    <td>CC4E4EN</td>
  </tr>
</table>

## IBM Cloud Pak for Multicloud Management 1.2용 Red Hat 소프트웨어 설치를 위한 IBM Red Hat 안내서
{: #rhinstall}

이 안내서에서는 Red Hat 소프트웨어를 빠르고 쉽게 설치하는 방법을 제공합니다. 

IBM Cloud Pak for Multicloud Management는 Red Hat OpenShift Container Platform, Red Hat Enterprise Linux CoreOS(RHCOS) 및 Red Hat Enterprise Linux(RHEL)를 사용할 수 있는 인타이틀먼트를 포함합니다. RHCOS는 OpenShift Container Platform 마스터 노드 호스트에 대해 유일하게 지원되는 운영 체제입니다. RHCOS 및 RHEL은 모두 OpenShift Container Platform 작업자 노드 호스트에 대해 지원되는 운영 체제이지만, 기본값은 RHCOS입니다. 

### Red Hat OpenShift Container Platform 설치

OpenShift Container Platform 4.x는 IBM 오퍼링에 대한 유료 Red Hat 구독 인타이틀먼트가 없어도 자유롭게 작성할 수 있는 Red Hat 계정을 사용해 Red Hat OpenShift Cluster Manager(https://cloud.redhat.com/openshift/install) 사이트에 액세스하여 다운로드하고 설치할 수 있습니다. 

Red Hat 계정이 없는 경우에는 나머지 지시사항을 따르기 전에 https://www.redhat.com/wapps/ugc/register.html 페이지에서 무료로 이를 작성하십시오. 

Red Hat 계정이 있는 경우에는 https://cloud.redhat.com/openshift/install 페이지로 이동해 자신의 계정 인증 정보를 사용하여 로그인하십시오. 

Cluster Manager가 다양한 클라우드 제공자 및 인프라 유형을 나타내는 몇 가지 타일을 표시합니다. OpenShift Container Platform을 설치할 인프라 유형에 대한 타일을 클릭하십시오. 일부 클라우드 제공자는 Cluster Manager가 자동으로 프로비저닝하는 클라우드 인프라에 OpenShift Container Platform을 설치하는 설치 프로그램 프로비저닝 인프라를 지원합니다. 그 외 클라우드 제공자 및 인프라 유형의 경우에는 사용자 프로비저닝 인프라에 클러스터를 설치할 수 있습니다. 

원하는 인프라 유형을 선택하고 `Installer-Provisioned Infrastructure` 또는 `User-Provisioned Infrastructure`를 선택한 후 표시되는 지시사항을 따르십시오. 

“베어메탈”타일을 비롯한 사용자 프로비저닝 인프라 유형의 경우에는 따라야 하는 일련의 짧은 단계가 표시됩니다. 자세한 설치 지시사항을 보려는 경우에는 “시작하기” 링크를 클릭하여 공식 설치 문서를 열 수 있습니다. “베어메탈” 인프라 유형의 경우에는 https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html 페이지의 문서를 참조하십시오. 

1. Cluster Manager 웹 사이트에서 제공하는 링크를 사용하여 OpenShift 설치 프로그램을 다운로드하십시오. 이러한 파일은 인터넷을 통해 직접 액세스할 수 있으며, 다운로드하는 데 Red Hat ID가 필요하지 않습니다. 
2. OpenShift 가져오기 시크릿을 다운로드하거나 복사하십시오. 이 단계를 수행하려면 Red Hat ID로 로그인한 상태여야 하지만 유료 구독이 필요하지는 않습니다. 
3. Cluster Manager 웹 사이트에서 제공하는 링크를 사용하여 Red Hat Enterprise Linux CoreOS(RHCOS)를 다운로드하십시오. 이러한 파일은 인터넷을 통해 직접 액세스할 수 있으며, 다운로드하는 데 Red Hat ID가 필요하지 않습니다. 
4. Cluster Manager 웹 사이트에서 제공하는 링크를 사용하여 OpenShift 명령행 도구(openshift-install)를 다운로드하고 이를 자신의 PATH에 추가하십시오. 이러한 파일은 인터넷을 통해 직접 액세스할 수 있으며, 다운로드하는 데 Red Hat ID가 필요하지 않습니다. 
5. 자신의 인프라 유형에 대한 공식 문서에 따라 openshift-install 명령을 사용하여 설치를 완료하십시오. 설치 프로그램이 완료되면 새 클러스터에 액세스하는 데 필요한 콘솔 URL 및 인증 정보가 표시됩니다. 또한 다운로드한 oc CLI 도구와 함께 사용할 kubeconfig 파일이 생성됩니다. 

<img src="red-hat-install.png" alt="IBM Passport Advantage에서 수동 설치를 위한 바이너리에 액세스하는 방법을 설명함">

### 선택사항: Red Hat Enterprise Linux 설치 바이너리 액세스

RHCOS는 OpenShift Container Platform 마스터 노드 호스트에 대해 유일하게 지원되는 운영 체제입니다. RHCOS 및 RHEL은 모두 OpenShift Container Platform 작업자 노드 호스트에 대해 지원되는 운영 체제이지만, 기본값은 RHCOS입니다. 작업자 노드 호스트에 Red Hat Enterprise Linux(RHEL)를 사용하려는 경우에는 RHEL 설치 2진 파일을 별도로 다운로드해야 하며, 이는 유료 인타이틀먼트 없이는 다운로드할 수 없습니다. 

바람직한 RHEL 액세스 및 설치 방법은 Red Hat의 표준 설치 문서를 따르고 Red Hat Network 구독을 사용하여 시스템을 등록하는 것입니다. 설치 2진 파일, 문서 및 인타이틀먼트 정보는 모두 Red Hat Customer Portal(https://access.redhat.com) 사이트에서 액세스할 수 있습니다. Red Hat Customer Portal을 처음 사용해보는 경우에는 로그인한 후 *시작하기*를 클릭하여(또는 링크 https://access.redhat.com/start/ 사용) 둘러보기 안내를 받고 Red Hat 구독을 최대한으로 활용하는 방법에 대해 알아보십시오. 

### 바람직한 RHEL 액세스 방법: Red Hat Customer Portal 사용

#### Red Hat Customer Portal을 사용한 설치 2진 파일 액세스

Cloud Pak 주문이 처리되고 나면 주문과 연관된 주소로 Red Hat의 이메일을 수신하게 됩니다. 이 이메일은 업데이트된 Red Hat OpenShift Container Platform 및 구독에 대한 인타이틀먼트 수량을 나열합니다. 

#### Red Hat Enterprise Linux 설치

OpenShift Container Platform 4.2는 Red Hat Enterprise Linux 7.6 이상에서 지원됩니다. 아직 Red Hat Enterprise Linux를 설치하지 않은 경우에는 다음 문서를 사용하여 Red Hat Enterprise Linux 설치를 완료하십시오. 

Red Hat Enterprise Linux 7.7 설치 매체는 Red Hat Customer Portal(https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software) 사이트를 통해 액세스할 수 있습니다. 

Subscription Manager를 사용한 설치 등록을 비롯한 Red Hat Enterprise Linux 7 다운로드 및 설치 지시사항은 Red Hat Customer Portal(https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started) 사이트에 있습니다. 

#### Red Hat OpenShift Container Platform 설치

Red Hat Enterprise Linux를 설치 및 등록하고 호스트 또는 가상 머신을 프로비저닝한 후에는 Red Hat Customer Portal(https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index) 사이트에 제공된 문서에 따라 OpenShift Container Platform 4.2 설치를 진행하십시오. 

### 다른 RHEL 액세스 방법: IBM Passport Advantage 사용

#### IBM Passport Advantage에서 수동 설치를 위한 2진 파일에 액세스

Red Hat Customer Portal에서 인타이틀먼트가 업데이트되기 전에 Cloud Pak을 설치해야 하는 경우, Red Hat OpenShift Container Platform 및 Red Hat Enterprise Linux CoreOS를 설치하는 데 필요한 모든 2진 파일은 이전에 설명한, 무료로 사용 가능한 Red Hat ID를 사용하여 다운로드할 수 있습니다. 이러한 2진 파일은 IBM Passport Advantage에서 다운로드할 수 없습니다. 

활성 Red Hat 구독이 없는 상태에서 작업자 노드에 호스트 운영 체제로 Red Hat Enterprise Linux를 설치하도록 선택하는 경우에는 IBM Passport Advantage를 통해 Red Hat Enterprise Linux 7.7에 액세스할 수 있습니다. Red Hat Enterprise Linux 7.7의 설치 이미지 및 RPM은 IBM Passport Advantage에서 다운로드할 수 있으며(부품 번호 CC4KJEN), 이는 Cloud Pak eAssembly의 일부입니다. IBM Passport Advantage에는 이 파일에 대해 “IBM Red Hat Enterprise Linux English only eImage” 라는 설명이 있습니다. 이 설치는 나중에 Red Hat Network ID에 등록하여 이와 연관시켜야 합니다. 

다운로드 용량은 약 50GB이며, 파일의 압축을 풀 때는 추가 스토리지가 필요합니다. 

이 수동 설치 프로세스를 위해서는 언급된 다운로드 패키지에 제공된 RPM 파일을 호스팅할 로컬 HTTP 서버를 작성해야 합니다. 바람직한 설치 방법 시나리오에서는 Red Hat Network를 통해 필요한 파일에 액세스할 수 있으므로 이러한 단계가 필요하지 않습니다. 

수동 설치를 수행하려면 다음 프로시저를 따르십시오. 

1. Passport Advantage에서 Red Hat Enterprise Linux 설치 파일을 다운로드(아직 Red Hat Enterprise Linux를 설치하지 않은 경우)
2. Yum 저장소를 호스팅할 웹 서버를 프로비저닝
3. 다운로드한 파일을 웹 서버에 복사
4. 작업자 노드에 Red Hat Enterprise Linux를 설치
5. 공식 문서를 사용하여 OpenShift Container Platform을 설치

#### Passport Advantage에서 Red Hat Enterprise Linux 설치 파일을 다운로드

IBM Passport Advantage에 로그인하여 Cloud Pak eAssembly와 연관된 “IBM Red Hat Enterprise Linux English only eImage”(부품 번호 CC4KJEN)를 다운로드하십시오. 다운로드할 파일 이름은 `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`입니다. 

#### Yum 저장소를 호스팅할 웹 서버를 프로비저닝

실제 호스트 또는 가상 머신을 로컬 설치를 지원할 HTTP 서버와 함께 프로비저닝하십시오. 원하는 웹 서버를 저장소로 사용할 수 있습니다. 

사용 가능한 웹 서버가 없는 경우에는 Red Hat에서 제공한 https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server 문서에서 표제 “Prepare and populate the repository server” 아래의 내용을 사용하여 Red Hat Enterprise Linux 시스템에 Apache 웹 서버를 설치하고 구성할 수 있습니다. 

#### 다운로드한 파일을 웹 서버에 복사

`IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`를 웹 서버에 복사하고 웹 서버의 문서 루트 아래에 있는 서브디렉토리 “repos”(문서를 사용하여 웹 서버를 작성한 경우에는 /var/www/html/repos)에 압축을 푸십시오. 

모든 사용자가 저장소 파일을 읽을 수 있도록 하십시오(chmod -R +r /var/www/html/repos). 

### 작업자 노드에 Red Hat Enterprise Linux를 설치

아직 Red Hat Enterprise Linux를 설치하지 않은 경우에는 Cloud Pak을 설치하는 OpenShift Container Platform 클러스터의 마스터 및 작업자 노드에 사용되는 호스트 또는 VM을 프로비저닝하고, IBM Passport Advantage에서 다운로드한 ISO를 사용하여 Red Hat Enterprise Linux를 설치하십시오. 

전제조건 및 호스트 준비를 비롯한 전체 Red Hat Enterprise Linux 다운로드 및 설치 지시사항은 Red Hat Customer Portal(https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started) 사이트에 있습니다. 

* 설치 매체의 ISO 이미지(rhel-server-7.7-x86_64-dvd.iso)는 IBM Passport Advantage에서 다운로드한 파일의 압축을 푼 디렉토리에 있습니다. 이러한 파일을 Red Hat Customer Portal에서 Red Hat Enterprise Linux를 다운로드하는 것을 설명하는 Red Hat Enterprise Linux 설치 안내서의 2장에 있는 단계에서 사용하십시오. 노드를 프로비저닝할 가상 머신을 작성하는 경우에는 이 이미지를 직접 사용할 수 있습니다. 
* Red Hat Enterprise Linux를 실제 호스트에 설치하는 경우에는 Red Hat Enterprise Linux 설치 안내서의 3장에서 실제 설치 매체 작성 또는 네트워크를 통한 설치 매체 액세스에 대한 정보를 참조하십시오(https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media). 

#### 공식 문서를 사용하여 Red Hat OpenShift Container Platform을 설치

Red Hat에서 제공한 https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index 문서에 따라 OpenShift Container Platform 4.2를 설치하십시오. 


## 저작권 및 상표 정보
{: #notices}

© Copyright IBM Corporation 2019

U.S. Government Users Restricted Rights - Use, duplication or disclosure restricted by GSA ADP Schedule Contract with IBM Corp.

IBM®, IBM 로고 및 ibm.com®은 전세계 여러 국가에 등록된 International Business Machines Corp.의 상표입니다. 기타 제품 및 서비스 이름은 IBM 또는 타사의 상표입니다. 현재 IBM 상표 목록은
웹 "저작권 및 상표 정보"(http://www.ibm.com/legal/copytrade.shtml) 페이지에 있습니다.
