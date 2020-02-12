# IBM Cloud Pak for Multicloud Management 1.2 クイック・スタート・ガイド (Red Hat OpenShift ガイダンス付き)

<b>製品リリース</b>: 1.2.0

<b>公開日</b>: 2019 年 12 月 13 日

<b>最終更新日</b>: 2019 年 12 月 6 日

このガイドは製品を使い始め、実行するための手早く簡単な方法を提供します。

## 説明
{: #desc}

IBM Cloud Pak for Multicloud Management は、Red Hat OpenShift 上で稼働し、オンプレミスからエッジに至るまで一貫性のある可視性、ガバナンス、および自動化を提供します。 企業は、マルチクラスター管理、イベント管理、アプリケーション管理、インフラストラクチャー管理、および既存ツール管理などの機能を利用できます。 さらに、この IBM Cloud Pak を使用して、インテリジェントなデータ、分析および予測された「ゴールデン・シグナル」によって運用効率を向上させ、コンプライアンス管理についてビルトインのサポートを受けることができます。

## 目次
{: #contents}

 1. [ユーザー向けオンライン資料](#docs)
 2. [インストール](#install)
 3. [ファイル・リスト](#files)
 4. [IBM Red Hat インストール・ガイド](#rhinstall)
 5. [著作権および商標](#notices)

## ユーザー向けオンライン資料
{: #docs}

最新の IBM Cloud Pak for Multicloud Management のユーザー向け資料については、https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html を参照してください。

## インストール
{: #install}

IBM Cloud Pak for Multicloud Management のインストールに関する最新の資料およびインストールの準備方法については、https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html を参照してください。

IBM シングル・サインオンを使用した Red Hat Ansible Tower の構成については、https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html を参照してください。

IBM シングル・サインオンを使用した Red Hat CloudForms の構成については、https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html を参照してください。

## ファイル・リスト
{: #files}

このセクションでは、バンドル用に IBM パスポート・アドバンテージで入手できるファイルのリストを提示します。

表 1. IBM Cloud Pak for Multicloud Management コア・パッケージ
<table border="1" width="100%">
  <tr>
    <th width="50%">説明</th>
    <th width="30%">ファイル名<br></th>
    <th width="20%">パスポート・アドバンテージ部品番号<br></th>
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

表 2. IBM Red Hat Software for IBM Cloud Pak for Multicloud Management パッケージ
<table border="1" width="100%">
  <tr>
    <th width="50%">説明</th>
    <th width="50%">パスポート・アドバンテージ部品番号<br></th>
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

表 3. IBM Cloud App Management for IBM Cloud Pak for Multicloud Management パッケージ
<table border="1" width="100%">
  <tr>
    <th width="50%">説明</th>
	<th width="30%">ファイル名<br></th>
    <th width="20%">パスポート・アドバンテージ部品番号<br></th>
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

 表 4. IBM Cloud App Management Extension Pack for IBM Cloud Pak for Multicloud Management パッケージ
<table border="1" width="100%">
  <tr>
    <th width="50%">説明</th>
	<th width="30%">ファイル名<br></th>
    <th width="20%">パスポート・アドバンテージ部品番号<br></th>
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

表 5. IBM Cloud Automation Manager パッケージ
<table border="1" width="100%">
  <tr>
    <th width="50%">説明</th>
    <th width="30%">ファイル名<br></th>
    <th width="20%">パスポート・アドバンテージ部品番号<br></th>
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

## IBM Cloud Pak for Multicloud Management 1.2 用の Red Hat ソフトウェアのインストールに関する IBM Red Hat ガイド
{: #rhinstall}

このガイドでは、Red Hat ソフトウェアをインストールするための手早く簡単な方法を説明します。

IBM Cloud Pak for Multicloud Management には、Red Hat OpenShift Container Platform、Red Hat Enterprise Linux CoreOS (RHCOS)、および Red Hat Enterprise Linux (RHEL) を使用するためのライセンスが組み込まれています。RHCOS は、OpenShift Container Platform マスター・ノードのホスト用にサポートされている唯一のオペレーティング・システムです。RHCOS と RHEL は、両方とも、OpenShift Container Platform ワーカー・ノードのホスト用にサポートされているオペレーティング・システムですが、RHCOS がデフォルトです。

### Red Hat OpenShift Container Platform のインストール

Red Hat OpenShift Cluster Manager (https://cloud.redhat.com/openshift/install) に Red Hat アカウントを使用してアクセスすることによって、OpenShift Container Platform 4.x をダウンロードおよびインストールすることができます。Red Hat アカウントは自由に作成でき、IBM オファリングへの有料 Red Hat サブスクリプション・ライセンスは必要ありません。

まだ Red Hat アカウントをお持ちでない場合は、https://www.redhat.com/wapps/ugc/register.html で無料で作成した後、残りの指示に従ってください。

Red Hat アカウントをお持ちの場合は、https://cloud.redhat.com/openshift/install にナビゲートし、アカウント資格情報を使用してログインしてください。

各種のクラウド・プロバイダーおよびインフラストラクチャー・タイプを表すいくつかのタイルがクラスター・マネージャーによって表示されます。OpenShift Container Platform をインストールするインフラストラクチャーのタイプに応じてタイルをクリックします。一部のクラウド・プロバイダーは Installer-Provisioned Infrastructure (インストーラーによってプロビジョンされるインフラストラクチャー) をサポートしていて、Cluster Manager によって自動的にプロビジョンされるクラウド・インフラストラクチャーに OpenShift Container Platform がインストールされます。他のクラウド・プロバイダーおよびインフラストラクチャー・タイプの場合、User-Provisioned Infrastructure (ユーザーによってプロビジョンされるインフラストラクチャー) にクラスターをインストールできます。

希望するインフラストラクチャー・タイプを選択し、`Installer-Provisioned Infrastructure` または `User-Provisioned Infrastructure` のいずれかを選択し、表示される指示に従ってください。

User-Provisioned Infrastructure タイプ (「ベアメタル」タイルを含む) の場合、示される短い一連のステップに従う必要があります。「Get Started」リンクをクリックして公式インストール資料を開くことによって、詳しいインストール指示を確認できます。「ベアメタル」インフラストラクチャー・タイプの場合、資料 https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html を参照してください。

1. Cluster Manager Web サイトで提供されるリンクを使用して OpenShift インストーラーをダウンロードします。これらのファイルはインターネットを介して直接アクセス可能であり、ダウンロードのために Red Hat ID は必要ありません。
2. OpenShift プル秘密をダウンロードまたはコピーします。このステップでは、Red Hat ID でログインしている必要がありますが、有料サブスクリプションは必要ありません。
3. Cluster Manager Web サイトで提供されるリンクを使用して Red Hat Enterprise Linux CoreOS (RHCOS) をダウンロードします。これらのファイルはインターネットを介して直接アクセス可能であり、ダウンロードのために Red Hat ID は必要ありません。
4. Cluster Manager Web サイトで提供されるリンクを使用して OpenShift コマンド・ライン・ツールをダウンロードし (openshift-install)、それらを PATH に追加します。これらのファイルはインターネットを介して直接アクセス可能であり、ダウンロードのために Red Hat ID は必要ありません。
5. インフラストラクチャー・タイプに合った公式資料に従い、openshift-install コマンドを使用してインストールを実行します。インストーラーが完了すると、コンソール URL と、新規クラスターにアクセスするための資格情報が表示されます。ダウンロードした oc CLI ツールで使用するための kubeconfig ファイルも生成されます。

<img src="red-hat-install.png" alt="IBM パスポート・アドバンテージからの手動インストール用バイナリーへのアクセスを説明しています">

### オプション: Red Hat Enterprise Linux インストール・バイナリーへのアクセス

RHCOS は、OpenShift Container Platform マスター・ノードのホスト用にサポートされている唯一のオペレーティング・システムです。RHCOS と RHEL は、両方とも、OpenShift Container Platform ワーカー・ノードのホスト用にサポートされているオペレーティング・システムですが、RHCOS がデフォルトです。Red Hat Enterprise Linux (RHEL) をワーカー・ノードのホスト用のオペレーティング・システムとして使用したい場合、RHEL インストール・バイナリー・ファイルは有料ライセンスがないとダウンロードできないため、それらのファイルを別個にダウンロードする必要があります。

RHEL にアクセスしてインストールするための推奨方法は、Red Hat からの標準インストール資料に従い、Red Hat Network サブスクリプションを使用してシステムを登録することです。インストール・バイナリー・ファイル、資料、およびライセンス情報のすべてに、Red Hat カスタマー・ポータル (https://access.redhat.com) からアクセスできます。Red Hat カスタマー・ポータルに初めてアクセスする場合、ログインした後、*「Getting Started」*をクリックして (または、リンク: https://access.redhat.com/start/ を使用して)、ガイド付きツアーを実行し、Red Hat サブスクリプションを最大限に活用する方法を学習してください。

### RHEL にアクセスするための推奨方法: Red Hat カスタマー・ポータルの使用

#### Red Hat カスタマー・ポータルを介したインストール・バイナリー・ファイルへのアクセス

Cloud Pak の注文が処理されると、注文に関連付けられたアドレスに Red Hat から E メールが届きます。この E メールには、Red Hat OpenShift Container Platform のライセンス数量がリストされ、サブスクリプションが更新されたことが示されます。

#### Red Hat Enterprise Linux のインストール

OpenShift Container Platform 4.2 は、Red Hat Enterprise Linux 7.6 以降でサポートされます。まだ Red Hat Enterprise Linux がインストールされていない場合、以下の資料を使用して Red Hat Enterprise Linux のインストールを実行してください。

Red Hat Enterprise Linux 7.7 インストール・メディアには、Red Hat カスタマー・ポータルを介してアクセスできます (https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software)。

Red Hat Enterprise Linux 7 のダウンロードおよびインストールに関する指示 (Subscription Manager を使用したインストールの登録を含む) は、Red Hat カスタマー・ポータルにあります (https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started)。

#### Red Hat OpenShift Container Platform のインストール

Red Hat Enterprise Linux がインストールおよび登録されたホストまたは仮想マシンのプロビジョンが成功したら、Red Hat カスタマー・ポータルにある資料 (https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index) に従って、OpenShift Container Platform 4.2 をインストールします。

### RHEL にアクセスするための代替方法: IBM パスポート・アドバンテージの使用

#### IBM パスポート・アドバンテージからの手動インストール用バイナリー・ファイルへのアクセス

Red Hat カスタマー・ポータルでライセンスが更新されるより前に Cloud Pak をインストールできる必要がある場合、Red Hat OpenShift Container Platform および Red Hat Enterprise Linux CoreOS をインストールするために必要なすべてのバイナリー・ファイルを、前述のように無料で使用可能な RED Hat ID を使用してダウンロードできます。これらのバイナリー・ファイルは、IBM パスポート・アドバンテージからはダウンロードできません。

アクティブな Red Hat サブスクリプションをまだ持っておらず、先に Red Hat Enterprise Linux をワーカー・ノード上のホスト・オペレーティング・システムとしてインストールすることを選択した場合、Red Hat Enterprise Linux 7.7 は IBM パスポート・アドバンテージを介してアクセス可能です。Red Hat Enterprise Linux 7.7 のインストール・イメージおよび RPM を IBM パスポート・アドバンテージからダウンロードできます (部品番号 CC4KJEN (これは Cloud Pak eAssembly の一部です))。IBM パスポート・アドバンテージでのこのファイルの説明は「IBM Red Hat Enterprise Linux English only eImage」です。このインストールは、後で、登録され、Red Hat Network ID と関連付けられる必要があります。

ダウンロードは約 50 GB であり、ファイルを解凍するときに余分にストレージが必要です。

この手動インストール処理には、前述のダウンロード・パッケージに入って提供される RPM ファイルをホストするためのローカル HTTP サーバーの作成が必要です。これらのステップは、推奨インストール方法を使用する場合は必要ありません。その場合のシナリオでは必要なファイルには Red Hat Network を介してアクセスすることが可能になるためです。

手動インストールを実行するには、以下の手順に従います。

1. パスポート・アドバンテージから Red Hat Enterprise Linux インストール・ファイルをダウンロードする (まだ Red Hat Enterprise Linux をインストールしていない場合)
2. Yum リポジトリーをホストするための Web サーバーをプロビジョンする
3. ダウンロードしたファイルを Web サーバーにコピーする
4. ワーカー・ノードに Red Hat Enterprise Linux をインストールする
5. 公式資料を使用して OpenShift Container Platform をインストールする

#### パスポート・アドバンテージからの Red Hat Enterprise Linux インストール・ファイルのダウンロード

IBM パスポート・アドバンテージにログインし、Cloud Pak eAssembly と関連付けられている「IBM Red Hat Enterprise Linux English only eImage」(部品番号 CC4KJEN) をダウンロードします。ダウンロードするファイルの名前は `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` です。

#### Yum リポジトリーをホストするための Web サーバーのプロビジョン

ローカル・インストールをサポートするための HTTP サーバーのある物理ホストまたは仮想マシンをプロビジョンします。任意の Web サーバーをリポジトリーとして使用できます。

使用可能な Web サーバーがない場合、Red Hat が提供する「Prepare and populate the repository server」という見出しの資料 (https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server) を使用して、Apache Web サーバーを Red Hat Enterprise Linux システムにインストールして構成することができます。

#### ダウンロードしたファイルの Web サーバーへのコピー

`IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` を Web サーバーにコピーし、Web サーバーの文書ルートの下の「repos」という名前のサブディレクトリー (資料を使用して Web サーバーを作成した場合は /var/www/html/repos) に解凍します。

リポジトリー・ファイルを任意のユーザーが読み取ることができることを確認します (chmod -R +r /var/www/html/repos)。

### ワーカー・ノードへの Red Hat Enterprise Linux のインストール

まだ Red Hat Enterprise Linux をインストールしていない場合、Cloud Pak をインストールする OpenShift Container Platform クラスターのマスター・ノードおよびワーカー・ノード用に使用されるホストまたは VM をプロビジョンし、IBM パスポート・アドバンテージからダウンロードされた ISO を使用して Red Hat Enterprise Linux をインストールします。

Red Hat Enterprise Linux のダウンロードおよびインストールの実行に関する指示 (前提条件およびホストの準備を含む) は Red Hat カスタマー・ポータルにあります (https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started)。

* IBM パスポート・アドバンテージからダウンロードしたファイルを解凍したディレクトリーに、インストール・メディアの ISO イメージ (rhel-server-7.7-x86_64-dvd.iso) があります。これらのファイルを、Red Hat カスタマー・ポータルからの Red Hat Enterprise Linux のダウンロードについて記述している Red Hat Enterprise Linux インストール・ガイドの第 2 章のステップの代わりに使用します。ノードをプロビジョンするための仮想マシンを作成している場合、このイメージを直接使用できます。
* Red Hat Enterprise Linux を物理ホストにインストールしている場合、Red Hat Enterprise Linux インストール・ガイドの第 3 章で、物理インストール・メディアの作成またはネットワークを介したインストール・メディアへのアクセスに関する情報を参照してください (https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media)。

#### 公式資料を使用した Red Hat OpenShift Container Platform のインストール

Red Hat が提供する資料に従って、OpenShift Container Platform 4.2 をインストールします (https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index)。


## 著作権および商標
{: #notices}

© Copyright IBM Corporation 2019



IBM、IBM ロゴおよび ibm.com は、世界の多くの国で登録された International Business Machines Corporation の商標です。 他の製品名およびサービス名等は、それぞれ IBM または各社の商標である場合があります。 現時点での IBM の商標リストについては、http://www.ibm.com/legal/copytrade.shtml をご覧ください。
