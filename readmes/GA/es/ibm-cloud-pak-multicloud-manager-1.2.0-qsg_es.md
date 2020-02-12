# Guía de inicio de rápido de IBM Cloud Pak for Multicloud Management 1.2 con Red Hat OpenShift Guidance

<b>Release del producto</b>: 1.2.0

<b>Fecha de publicación</b>: 13 de diciembre de 2019

<b>Fecha de última modificación</b>: 6 de diciembre de 2019

Esta guía proporciona una forma rápida y fácil de activar y ejecutar el producto.

## Descripción
{: #desc}

IBM Cloud Pak for Multicloud Management, ejecutándose en Red Hat OpenShift, proporciona visibilidad, gobierno y automatización
desde sistemas locales hasta periféricos. Las empresas obtienen funciones, tales como gestión multiclúster, gestión de sucesos, gestión de aplicaciones, gestión de infraestructuras y gestión de herramientas existentes. Las empresas pueden utilizar este IBM Cloud Pak para mejorar la eficiencia operativa utilizando el análisis de datos inteligentes y señales doradas predictivas, y acceder a soporte incorporado para la gestión de conformidad.

## Contenido
{: #contents}

 1. [Documentación de usuario en línea](#docs)
 2. [Instalación ](#install)
 3. [Lista de archivos](#files)
 4. [Guía de instalación de IBM Red Hat](#rhinstall)
 5. [Información de copyright y marcas registradas](#notices)

## Documentación de usuario en línea
{: #docs}

Para obtener la documentación de usuario más reciente de IBM Cloud Pak for Multicloud Management, consulte: https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/kc_welcome_cloud_pak.html.

## Instalación
{: #install}

Para obtener la documentación de instalación de IBM Cloud Pak for Multicloud Management más reciente y para obtener información sobre cómo preparar la instalación, consulte: https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/overview.html.

Para obtener información sobre cómo configurar Red Hat Ansible Tower con inicio de sesión único de IBM, consulte: https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/ansible_tower.html.

Para obtener información acerca de cómo configurar Hat CloudForms con inicio de sesión único de IBM, consulte: https://www.ibm.com/support/knowledgecenter/SSFC4F_1.2.0/install/cloudforms.html.

## Lista de archivos
{: #files}

En esta sección se muestra una lista de los archivos disponibles en IBM Passport Advantage para su paquete. 

Tabla 1. Paquetes de IBM Cloud Pak for Multicloud Management Core
<table border="1" width="100%">
  <tr>
    <th width="50%">Descripción</th>
    <th width="30%">Nombre de archivo<br></th>
    <th width="20%">Número de pieza de Passport Advantage<br></th>
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

Tabla 2. Paquetes de IBM Red Hat Software for IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
  <tr>
    <th width="50%">Descripción</th>
    <th width="50%">Número de pieza de Passport Advantage<br></th>
  </tr>
  <tr>
    <td>IBM Red Hat Enterprise Linux 7.7 English Only </td>
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

Tabla 3. Paquetes de IBM Cloud App Management for IBM Cloud Pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Descripción</th>
	<th width="30%">Nombre de archivo</th>
    <th width="20%">Número de pieza de Passport Advantage<br></th>
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
  </table>

 Tabla 4. Paquetes de IBM Cloud App Management Extension Pack for IBM Cloud pak for Multicloud Management
<table border="1" width="100%">
 <tr>
    <th width="50%">Descripción</th>
	<th width="30%">Nombre de archivo</th>
    <th width="20%">Número de pieza de Passport Advantage<br></th>
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

Tabla 5. Paquetes de IBM Cloud Automation Manager
<table border="1" width="100%">
  <tr>
    <th width="50%">Descripción</th>
    <th width="30%">Nombre de archivo<br></th>
    <th width="20%">Número de pieza de Passport Advantage<br></th>
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

## IBM Red Hat - Guía de instalación de Red Hat Software for IBM Cloud Pak for Multicloud Management 1.2
{: #rhinstall}

Esta guía proporciona una forma rápida y fácil de instalar el software de Red Hat. 

IBM Cloud Pak for Multicloud Management incluye la titularidad de uso de Red Hat OpenShift Container Platform, Red Hat Enterprise Linux CoreOS (RHCOS) y Red Hat Enterprise Linux (RHEL). RHCOS es el único sistema operativo soportado para los hosts de nodo maestro de OpenShift Container Platform. Tanto RHCOS como RHEL son sistemas operativos soportados para los hosts de nodos de trabajador de OpenShift Container Platform, aunque RHCOS es el valor predeterminado. 

### Instalación de Red Hat OpenShift Container Platform

Puede descargar e instalar OpenShift Container Platform 4.x accediendo a Red Hat OpenShift Cluster Manager en https://cloud.redhat.com/openshift/install, utilizando su cuenta de Red Hat, que puede crear gratuitamente, sin una titularidad de suscripción de Red Hat de pago para cualquier oferta de IBM.

Si todavía no tiene una cuenta de Red Hat, cree una gratuitamente en: https://www.redhat.com/wapps/ugc/register.html, antes de seguir las instrucciones restantes. 

Si tiene una cuenta de Red Hat, vaya a: https://cloud.redhat.com/openshift/install e inicie sesión con las credenciales de su cuenta.

El gestor del clúster muestra varios mosaicos que representan diferentes proveedores de nube y tipos de infraestructuras. Pulse el mosaico del tipo de infraestructura donde desea instalar OpenShift Container Platform. Algunos proveedores de nube dan soporte a la infraestructura suministrada por el instalador, el cual instala OpenShift Container Platform en la estructura de nube que suministra automáticamente el gestor del clúster. Para otros proveedores de nube y tipos de infraestructuras, se puede instalar un clúster en la infraestructura suministrada por el usuario.

Seleccione el tipo de infraestructura que prefiera y elija `Infraestructura suministrada por el instalador` o `Infraestructura suministrada por el usuario`, a continuación, siga las instrucciones que se muestran.

Para cualquiera de los tipos de infraestructura suministrada por el usuario, incluido el mosaico "Bare Metal" se le presentará una breve serie de pasos a seguir. Para obtener las instrucciones de instalación detalladas, puede pulsar el enlace “Iniciación” para abrir la documentación de instalación oficial. Para el tipo de infraestructura “Bare Metal”, consulte la documentación: https://docs.openshift.com/container-platform/4.2/installing/installing_bare_metal/installing-bare-metal.html.

1. Descargue el instalador de OpenShift utilizando el enlace que proporciona el sitio web del gestor del clúster. Se puede acceder directamente a estos archivos en internet y no se requiere un ID de Red Hat para su descarga.
2. Descargue o copie su secreto de extracción de OpenShift. Para este paso es necesario que inicie sesión con un ID de Red Hat pero no es necesaria una suscripción de pago.
3. Descargue RHCOS (Red Hat Enterprise Linux CoreOS) utilizando el enlace que proporciona el sitio web del gestor del clúster. Se puede acceder directamente a estos archivos en internet y no se requiere un ID de Red Hat para su descarga.
4. Descargue las herramientas de línea de mandatos de OpenShift (openshift-install) utilizando el enlace que proporciona el sitio web del gestor del clúster y añádalas a su PATH. Se puede acceder directamente a estos archivos en internet y no se requiere un ID de Red Hat para su descarga.
5. Siga la documentación oficial de su tipo de infraestructura para completar la instalación utilizando el mandato openshift-install. Cuando finaliza el instalador, puede ver el URL de la consola y las credenciales para acceder a su nuevo clúster. También se genera un archivo kubeconfig para que lo utilice con las herramientas oc de CLI que ha descargado.

<img src="red-hat-install.png" alt="Describe el acceso a binarios para la instalación manual desde IBM Passport Advantage">

### Opcional: Acceso a los binarios de instalación de Red Hat Enterprise Linux

RHCOS es el único sistema operativo soportado para los hosts de nodo maestro de OpenShift Container Platform. Tanto RHCOS como RHEL son sistemas operativos soportados para los hosts de nodos de trabajador de OpenShift Container Platform, aunque RHCOS es el valor predeterminado. Si prefiere utilizar RHEL (Red Hat Enterprise Linux) como el sistema operativo para los hosts de nodos de trabajador, necesita descargar los archivos binarios de instalación de RHEL por separado, ya que no están disponibles para su descarga sin una titularidad de pago.

El método preferido para acceder e instalar RHEL es seguir la documentación de instalación estándar de Red Hat y registrar sus sistemas utilizando su suscripción de Red Hat Network. Se puede acceder a los archivos binarios de instalación, la documentación y la información de titularidad desde Red Hat en: https://access.redhat.com. Si es nuevo en el portal del cliente de Red Hat, pulse *Iniciación* después de iniciar sesión (o utilice este enlace: https://access.redhat.com/start/) para realizar un recorrido guiado y aprender a obtener el máximo rendimiento de su suscripción de Red Hat. 

### Método preferido para acceder a RHEL: Utilizando el portal del cliente de Red Hat

#### Acceso a archivos binarios mediante el portal del cliente de Red Hat

Una vez procesado su pedido de Cloud Pak, recibirá un correo electrónico de Red Hat en la dirección asociada a su pedido. Este correo electrónico enumera la cantidad de titularidades de su Red Hat OpenShift Container Platform y le informa de que se ha actualizado su suscripción. 

#### Instalación de Red Hat Enterprise Linux

OpenShift Container Platform 4.2 está soportado en Red Hat Enterprise Linux 7.6 o posterior. Si todavía no tiene instalado Red Hat Enterprise Linux, utilice la documentación siguiente para completar la instalación de Red Hat Enterprise Linux.

Se puede acceder al soporte de instalación de Red Hat Enterprise Linux 7.7 a través del portal del cliente de Red Hat en: https://access.redhat.com/downloads/content/69/ver=/rhel---7/7.7/x86_64/product-software

Puede encontrar las instrucciones para descargar e instalar Red Hat Enterprise Linux 7, incluido el registro de su instalación, utilizando el gestor de suscripciones en el portal del cliente de Red Hat en: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

#### Instalación de Red Hat OpenShift Container Platform

Cuando haya suministrado correctamente los hosts o máquinas virtuales con Red Hat Enterprise Linux instalado y registrado, continúe con la instalación de OpenShift Container Platform 4.2 siguiendo las instrucciones de la documentación que se proporciona en el portal del cliente de Red Hat en: https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index

### Método alternativo para acceder a RHEL: utilizando IBM Passport Advantage

#### Acceso a los archivos binarios para la instalación manual desde IBM Passport Advantage

Si requiere que sea posible instalar Cloud Pak antes de que se actualicen sus titularidades en el portal del cliente de Red Hat, todos los archivos binarios necesarios para instalar Red Hat OpenShift Container Platform y Red Hat Enterprise Linux CoreOS están disponibles para su descarga utilizando un ID de Red Hat disponible gratuitamente, como se ha descrito anteriormente. Estos archivos binarios no están disponibles para su descarga desde IBM Passport Advantage.

Si opta por instalar antes Red Hat Enterprise Linux como el sistema operativo de sus nodos de trabajador y todavía no tiene una suscripción de Red Hat activa, Red Hat Enterprise Linux 7.7 está accesible desde IBM Passport Advantage. Las imágenes de instalación y los RPM para Red Hat Enterprise Linux 7.7 se pueden descargar desde IBM Passport Advantage (Número de pieza CC4KJEN), que forma parte de su Cloud Pak eAssembly. Este archivo se describe como “IBM Red Hat Enterprise Linux English only eImage” en IBM Passport Advantage. Esta instalación requiere que esté registrado y asociado a su ID de Red Hat Network posteriormente. 

Aproximadamente la descarga es de 50 GB, y se requiere almacenamiento adicional cuando extrae los archivos.

Este proceso de instalación manual requiere crear un servidor HTTP local para alojar los archivos RPM que se proporcionan en el paquete de descarga mencionado. Estos pasos no son necesarios cuando utiliza el método de instalación preferido, ya que este caso de uso permite acceder a los archivos necesarios mediante Red Hat Network.

Para realizar una instalación manual, siga este procedimiento: 

1. Descargue los archivos de instalación de Red Hat Enterprise Linux desde Passport Advantage (si todavía no ha instalado Red Hat Enterprise Linux)
2. Suministre un servidor web para alojar un repositorio Yum 
3. Copie los archivos descargados en el servidor web 
4. Instale Red Hat Enterprise Linux en los nodos de trabajador 
5. Instale OpenShift Container Platform utilizando la documentación oficial 

#### Descargue los archivos de instalación de Red Hat Enterprise Linux desde Passport Advantage

Inicie sesión en IBM Passport Advantage y descargue "IBM Red Hat Enterprise Linux English only eImage" (número de pieza CC4KJEN), que está asociado a Cloud Pak eAssembly. El nombre del archivo a descargar es `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz`.

#### Suministre un servidor web para alojar un repositorio Yum 

Suministre un host físico o una máquina virtual con un servidor HTTP para dar soporte a la instalación local. Puede utilizar el servidor web de su elección como repositorio. 

Si no dispone de un servidor web, puede instalar y configurar el servidor web Apache en un sistema Red Hat Enterprise Linux utilizando la documentación que proporciona Red Hat bajo la cabecera "Preparar y rellenar el servidor de repositorio": https://docs.openshift.com/container-platform/3.11/install/disconnected_install.html#disconnected-repo-server

#### Copie los archivos descargados en el servidor web 

Copie `IBM_RED_HAT_ENTERPRISE_LINUX_ENGLISH.tgz` en el servidor web y extráigalo en un subdirectorio con el nombre "repos" en la raíz del documento del servidor web (/var/www/html/repos si ha creado un servidor web utilizando la documentación).

Asegúrese de que cualquier usuario pueda leer los archivos del repositorio (chmod -R +r /var/www/html/repos).

### Instale Red Hat Enterprise Linux en los nodos de trabajador 

Si todavía no tiene instalado Red Hat Enterprise Linux, suministre los hosts o máquinas virtuales (VM) que se utilizan para los nodos maestro o de trabajador para el clúster de OpenShift Container Platform donde instala Cloud Pak, e instale Red Hat Enterprise Linux utilizando el ISO descargado desde IBM Passport Advantage.

Siga las instrucciones de descarga e instalación de Red Hat Enterprise Linux, incluidos los requisitos previos y la preparación del host, que puede encontrar en el portal del cliente de Red Hat en: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-getting-started

* Puede encontrar una imagen ISO del soporte de instalación (rhel-server-7.7-x86_64-dvd.iso) en el directorio en que ha extraído el archivo descargado desde IBM Passport Advantage. Utilice estos archivos en lugar de los pasos del capítulo 2 de la guía de instalación de Red Hat Enterprise Linux que describe la descarga de Red Hat Enterprise Linux desde el portal del cliente de Red Hat. Si está creando máquinas virtuales para suministrar los nodos, esta imagen se puede utilizar directamente.
* Si está instalando Red Hat Enterprise Linux en un host físico, consulte el capítulo 3 de la guía de instalación de Red Hat Enterprise Linux para obtener información sobre cómo crear un soporte de instalación físico o para acceder al soporte de instalación a través de una red: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/chap-making-media

#### Instale Red Hat OpenShift Container Platform utilizando la documentación oficial 

Siga las indicaciones de la documentación que proporciona Red Hat para instalar OpenShift Container Platform 4.2: https://access.redhat.com/documentation/en-us/openshift_container_platform/4.2/html-single/installing/index


## Información de copyright y marcas registradas
{: #notices}

© Copyright IBM Corporation 2019

Derechos restringidos para los usuarios del gobierno de los EE.UU. - Uso, duplicación o divulgación restringidos por el GSA ADP Schedule Contract con IBM Corp.

IBM, el logotipo de IBM e ibm.com son marcas registradas de International Business Machines Corp., registradas en muchas jurisdicciones en todo el mundo. Otros nombres de productos y servicios pueden ser marcas registradas de IBM o de otras empresas. Encontrará la lista actual de las marcas comerciales de IBM en el sitio web "Información de copyright y marcas registradas" en la dirección www.ibm.com/legal/copytrade.shtml.
