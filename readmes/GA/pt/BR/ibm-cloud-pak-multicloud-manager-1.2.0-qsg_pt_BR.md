# Guia de iniciação rápida do IBM Cloud Pak for Multicloud Management 1.2 com orientação do Red Hat OpenShift

<b>Liberação do produto</b>: 1.2.0

<b>Data de publicação</b>: 13 de dezembro de 2019

<b>Data da última modificação</b>: 6 de dezembro de 2019

Este guia fornece uma maneira rápida e fácil de ter o produto funcionando.

## Descrição
{: #desc}

O IBM Cloud Pak for Multicloud Management, em execução no Red Hat OpenShift, fornece visibilidade, controle e automação consistentes das instalações até a borda. As empresas ganham recursos como gerenciamento de vários clusters, gerenciamento de eventos, gerenciamento de aplicativos, gerenciamento de infraestrutura e gerenciamento das ferramentas existentes. As empresas podem usar esse IBM Cloud Pak para ajudar a aumentar a eficiência operacional que é orientada por dados inteligentes, análise e sinais de ouro preditivos, além de ganhar suporte integrado para seu gerenciamento de conformidade.

## Índice
{: #contents}

 1. [Documentação do usuário on-line](#docs)
 2. [Pôster de](#install)
 3. [Lista dos arquivos](#files)
 4. [Guia de instalação do IBM Red Hat](#rhinstall)
 5. [Informações de Copyright e Marca Comercial](#notices)

## Documentação do usuário on-line
{: #docs}

Para obter a documentação do usuário mais atualizada do IBM Cloud Pak for Multicloud Management, consulte https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html.

## Pôster de
{: #install}

Para obter a documentação de instalação recente do IBM Cloud Pak for Multicloud Management e saber como se preparar para a instalação, consulte https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html.

Para obter informações sobre como configurar o Red Hat Ansible Tower com a conexão única da IBM, consulte https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html.

Para obter informações sobre como configurar o Red Hat CloudForms com a conexão única da IBM, consulte https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html.

## Lista dos arquivos
{: #files}

Esta seção lista os arquivos que estão disponíveis no IBM Passport Advantage para seu pacote configurável.

Tabela 1. Pacotes do IBM Cloud Pak for Multicloud Management Core
<table border="1" width="100%">
  <tr>
    <th width="50%">Descrição</th>
    <th width="30%">Nome do arquivo<br></th>
    <th width="20%">Número da peça do Passport Advantage<br></th>
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

Tabela 2. Pacotes do IBM Red Hat Software for IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
  <tr>
    <th width="50%">Descrição</th>
    <th width="50%">Número da peça do Passport Advantage<br></th>
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

Tabela 3. Pacotes do IBM Cloud App Management for IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Descrição</th>
	<th width="30%">Nome do arquivo<br></th>
    <th width="20%">Número da peça do Passport Advantage<br></th>
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

 Tabela 4. Pacotes do IBM Cloud App Management Extension Pack for IBM Cloud pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Descrição</th>
	<th width="30%">Nome do arquivo<br></th>
    <th width="20%">Número da peça do Passport Advantage<br></th>
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

Tabela 5. Pacotes do IBM Cloud Automation Manager
<table border="1" width="100%">
  <tr>
    <th width="50%">Descrição</th>
    <th width="30%">Nome do arquivo<br></th>
    <th width="20%">Número da peça do Passport Advantage<br></th>
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
    <td>IBM Cloud Automation Manager 4.1 for Power Linux LE (64 bits)</td>
    <td>icp-cam-ppc-3.2.2.tar.gz</td>
    <td>CC4E3EN</td>
  </tr>
  <tr>
    <td>IBM Cloud Automation Manager 4.1 Product ID</td>
    <td>icp-cam-prod-id-3.2.2.txt</td>
    <td>CC4E4EN</td>
  </tr>
</table>

## Guia do IBM Red Hat para instalação do Red Hat Software for IBM Cloud Pak for Multicloud Management 1.2
{: #rhinstall}

Este guia fornece uma maneira rápida e fácil de instalar o software Red Hat.

O IBM Cloud Pak for Multicloud Management inclui a autorização para usar o Red Hat OpenShift Container Platform, o Red Hat Enterprise Linux CoreOS (RHCOS) e o Red Hat Enterprise Linux (RHEL). O RHCOS é o único sistema operacional suportado para os hosts de nó principal do OpenShift Container Platform. Os sistemas operacionais RHCOS e RHEL são ambos suportados para os hosts de nó do trabalhador do OpenShift Container Platform, embora o RHCOS seja o padrão.

### Instalando o Red Hat OpenShift Container Platform

O OpenShift Container Platform 4.x pode ser transferido por download e instalado acessando o Red Hat OpenShift Cluster Manager em https://cloud.redhat.com/openshift/install utilizando a conta do Red Hat, que pode ser criada gratuitamente, sem o pagamento de uma autorização de assinatura do Red Hat para qualquer oferta da IBM.

Caso ainda não tenha uma conta do Red Hat, crie uma gratuitamente em https://www.redhat.com/wapps/ugc/register.html antes de seguir as instruções restantes.

Se tiver uma conta do Red Hat, navegue para https://cloud.redhat.com/openshift/install e efetue login com suas credenciais de conta.

O gerenciador do cluster exibe vários ladrilhos, que representam diversos provedores em nuvem e tipos de infraestrutura. Clique no ladrilho do tipo de infraestrutura no qual você deseja instalar o OpenShift Container Platform. Alguns provedores em nuvem suportam o Installer-Provisioned Infrastructure, que instala o OpenShift Container Platform na estrutura em nuvem que é fornecida automaticamente pelo Cluster Manager. Para outros provedores em nuvem e tipos de infraestrutura, é possível instalar um cluster no User-Provisioned Infrastructure.

Selecione o tipo de estrutura de sua preferência e escolha `Installer-Provisioned Infrastructure` ou `User-Provisioned Infrastructure`, em seguida, siga as instruções exibidas.

Para qualquer um dos tipos de User-Provisioned Infrastructure, incluindo o ladrilho “Bare Metal”, será apresentada uma breve série de etapas a serem seguidas. Para obter instruções de instalação detalhadas, é possível clicar no link “Introdução” para abrir a documentação oficial de instalação. Para o tipo de infraestrutura “Bare Metal”, consulte a documentação: https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html.

1. Faça download do instalador do OpenShift, usando o link fornecido pelo website do Cluster Manager. Esses arquivos podem ser acessados diretamente por meio da Internet e seu download não requer um ID do Red Hat.
2. Faça download ou copie seu segredo de pull do OpenShift. Essa etapa requer o login com um ID do Red Hat, mas não requer uma assinatura paga.
3. Faça download do Red Hat Enterprise Linux CoreOS (RHCOS), usando o link fornecido pelo website do Cluster Manager. Esses arquivos podem ser acessados diretamente por meio da Internet e seu download não requer um ID do Red Hat.
4. Faça download do OpenShift Command Line Tools (openshift-install), usando o link fornecido pelo website do Cluster Manager e, em seguida, inclua-o em seu PATH. Esses arquivos podem ser acessados diretamente por meio da Internet e seu download não requer um ID do Red Hat.
5. Siga a documentação oficial para o tipo de infraestrutura para concluir a instalação, usando o comando openshift-install. Quando o instalador for concluído, você verá a URL do console e as credenciais para acessar o novo cluster. Também será gerado um arquivo kubeconfig para ser usado com as ferramentas de CLI do oc que foram transferidas por download.

<img src="red-hat-install.png" alt="Descreve como acessar os binários para instalação manual a partir do IBM Passport Advantage">

### Opcional: acessando os binários de instalação do Red Hat Enterprise Linux

O RHCOS é o único sistema operacional suportado para os hosts de nó principal do OpenShift Container Platform. Os sistemas operacionais RHCOS e RHEL são ambos suportados para os hosts de nó do trabalhador do OpenShift Container Platform, embora o RHCOS seja o padrão. Caso prefira usar o Red Hat Enterprise Linux (RHEL) como o sistema operacional para os hosts do nó do trabalhador, é necessário fazer download dos arquivos binários de instalação do RHEL separadamente, pois eles só ficam disponíveis para download mediante uma autorização paga.

O método preferencial para o acesso e a instalação do RHEL é seguir a documentação padrão de instalação do Red Hat e registrar os sistemas usando a assinatura do Red Hat Network. Os arquivos binários de instalação, a documentação e todas as informações de autorização podem ser acessados a partir do Red Hat Customer Portal em https://access.redhat.com. Se não estiver familiarizado com o Red Hat Customer Portal, clique em *Introdução* depois de efetuar login (ou use este link: https://access.redhat.com/start/) para fazer um tour guiado e aprender como aproveitar ao máximo sua assinatura do Red Hat.

### Método preferencial para acessar o RHEL: usando o Red Hat Customer Portal

#### Acessando os arquivos binários de instalação por meio do Red Hat Customer Portal

Depois que seu pedido do Cloud Pak for processado, você receberá um e-mail do Red Hat no endereço que está associado ao pedido. Esse e-mail lista as quantidades de autorização do Red Hat OpenShift Container Platform e assinatura é atualizada.

#### Instalando o
Red Hat Enterprise Linux

O OpenShift Container Platform 4.2 é suportado no Red Hat Enterprise Linux 7.6 ou mais recente. Caso ainda não tenha o Red Hat Enterprise Linux instalado, use a documentação a seguir para concluir a instalação do Red Hat Enterprise Linux.

A mídia de instalação do Red Hat Enterprise Linux 7.7 pode ser acessada por meio do Red Hat Customer Portal, em https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software

As instruções de download e instalação do Red Hat Enterprise Linux 7, incluindo o registro da instalação usando o Gerenciador de assinaturas, podem ser encontradas no Red Hat Customer Portal, em: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

#### Instalando o Red Hat OpenShift Container Platform

Depois de fornecer com êxito os hosts ou máquinas virtuais com o Red Hat Enterprise Linux instalado e registrado, continue com a instalação do OpenShift Container Platform 4.2, seguindo a documentação fornecida no Red Hat Customer Portal: https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index

### Método alternativo para acessar o RHEL: usando o IBM Passport Advantage

#### Acessando arquivos binários para instalação manual a partir do IBM Passport Advantage

Caso seja preciso instalar o Cloud Pak antes que suas autorizações tenham sido atualizadas no Red Hat Customer Portal, todos os arquivos binários necessários para a instalação do Red Hat OpenShift Container Platform e do Red Hat Enterprise Linux CoreOS podem ser transferidos por download usando um ID do Red Hat que é disponibilizado gratuitamente, conforme descrito anteriormente. Esses arquivos binários não estão disponíveis para download a partir do IBM Passport Advantage.

Se você optar por instalar antes o Red Hat Enterprise Linux como o sistema operacional host nos nós do trabalhador e ainda não tiver uma assinatura ativa do Red Hat, é possível acessar o Red Hat Enterprise Linux 7.7 por meio do IBM Passport Advantage. As imagens de instalação e RPMs para o Red Hat Enterprise Linux 7.7 podem ser transferidas por download a partir do IBM Passport Advantage (Número de peça CC4KJEN), que faz parte do Cloud Pak eAssembly. No IBM Passport Advantage, a descrição desse arquivo é “IBM Red Hat Enterprise Linux English only eImage”. Posteriormente, essa instalação precisa ser registrada e associada ao seu ID do Red Hat Network.

O download tem aproximadamente 50 GB e é necessário um armazenamento adicional ao extrair os arquivos.

Esse processo de instalação manual requer a criação de um servidor HTTP local para hospedar os arquivos RPM que são fornecidos no pacote de download mencionado. Essas etapas não são necessárias ao usar o método de instalação preferencial, uma vez que esse cenário permite o acesso aos arquivos necessários por meio do Red Hat Network.

Para executar uma instalação manual, siga este procedimento:

1. Faça download dos arquivos de instalação do Red Hat Enterprise Linux a partir do Passport Advantage (caso o Red Hat Enterprise Linux ainda não esteja instalado)
2. Forneça um servidor da web para hospedar um repositório Yum
3. Copie para o servidor da web os arquivos transferidos por download
4. Instale o Red Hat Enterprise Linux nos nós do trabalhador
5. Instale o OpenShift Container Platform usando a documentação oficial

#### Faça download dos arquivos de instalação do Red Hat Enterprise Linux a partir do Passport Advantage

Efetue login no IBM Passport Advantage e faça download de “IBM Red Hat Enterprise Linux English only eImage” (número de peça CC4KJEN), que está associado ao Cloud Pak eAssembly. O nome do arquivo de download é `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`.

#### Forneça um servidor da web para hospedar um repositório Yum

Forneça um host físico ou uma máquina virtual com um servidor HTTP para suportar a instalação local. Para o repositório, é possível usar o servidor da web de sua escolha.

Caso não haja um servidor da web disponível, é possível instalar e configurar o servidor da web Apache em um sistema Red Hat Enterprise Linux, usando a documentação que é fornecida pelo Red Hat com o título “Preparar e preencher o servidor do repositório”: https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server

#### Copie para o servidor da web os arquivos transferidos por download

Copie `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` para o servidor da web e extraia-o em um subdiretório chamado “repos”, contido na raiz do documento do servidor da web (que é /var/www/html/repos caso o servidor da web tenha sido criado usando a documentação).

Assegure-se de que os arquivos de repositório possam ser lidos por qualquer usuário (chmod -R +r /var/www/html/repos).

### Instale o Red Hat Enterprise Linux nos nós do trabalhador

Caso o Red Hat Enterprise Linux ainda não esteja instalado, forneça as MVs ou os hosts usados para os nós principal e do trabalhador para o cluster do OpenShift Container Platform no qual o Cloud Pak é instalado e instale o Red Hat Enterprise Linux usando a ISO que é transferida por download a partir do IBM Passport Advantage.

As instruções completas de download e instalação do Red Hat Enterprise Linux, incluindo pré-requisitos e preparação do host, podem ser encontradas no Red Hat Customer Portal, em: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

* Uma imagem ISO da mídia de instalação (rhel-server-7.7-x86_64-dvd.iso) pode ser encontrada no diretório no qual o arquivo transferido por download do IBM Passport Advantage foi extraído. Use esses arquivos no lugar das etapas do Capítulo 2 do guia de instalação do Red Hat Enterprise Linux, que descreve como fazer o download do Red Hat Enterprise Linux a partir do Red Hat Customer Portal. Caso esteja criando máquinas virtuais para fornecer os nós, é possível usar essa imagem diretamente.
* Se estiver instalando o Red Hat Enterprise Linux em um host físico, consulte o Capítulo 3 do guia de instalação do Red Hat Enterprise Linux para obter informações sobre como criar a mídia de instalação física ou como acessar a mídia de instalação por meio de uma rede: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media

#### Instale o Red Hat OpenShift Container Platform usando a documentação oficial

Siga a documentação fornecida pelo Red Hat para instalar o OpenShift Container Platform 4.2: https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index


## Informações de Copyright e Marca Comercial
{: #notices}

© Copyright IBM Corporation 2019

Direitos Restritos para Usuários do Governo dos Estados Unidos - Uso, duplicação e divulgação
restritos pelo documento GSA ADP Schedule Contract com a IBM Corporation.

IBM®, o logotipo IBM e ibm.com® são marcas comerciais da International Business Machines Corp., registradas em vários países no mundo todo. Outros nomes de produtos e serviços podem ser marcas registradas da IBM ou de terceiros. Uma lista atual de marcas registradas da IBM está disponível na Web em
"Copyright and trademark information" em www.ibm.com/legal/copytrade.shtml.
