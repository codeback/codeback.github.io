---
layout: default
title: Magento Integration
---

# Integración con tiendas Magento 1.9.x
### Compromiso Hoppin: ¡Integración en menos de 30 minutos! :alarm_clock:

En esta guía se describen los pasos para integrar tu tienda con **Hoppin**.


#### Paso 1: Subir el módulo Hoppin

Descarga el módulo aquí: [Descargar Módulo]({{ site.url }}/download/hoppin-magento.zip)

Sube el módulo al directorio raíz de tu instalación de Magento y descomprímelo. Este módulo creará un nuevo método de pago (llamado Hoppin) y hará que no se muestre en el *checkout* a los usuarios que compren de modo convencional en la web de la tienda.


#### Paso 2: Medida de precaución (Just in case)

* Crea una copia de seguridad desde *System->Tools->Backup*
* Deshabilita las compilaciones en *System->Tools->Compilations*
* Limpia la caché en *System -> Cache Management*

Ahora, sal de la sesión de administrador de Magento y accede de nuevo.


#### Paso 3: Configurar el módulo

Dirígete a *System->Configuration->Payment Methods*, encuentra el nuevo método de pago Hoppin y seleccionar el **New order status** que desees para los pedios que se generen desde Hoppin.

![magento-ss-01]({{ site.baseurl }}/images/magento-ss-01.png)


#### Paso 4: Configurar el acceso a través de la API: Crear un Rol de usuario con los permisos adecuados

Pulsa en *System->Web Services->SOAP/XML-RPC - Roles*.

![magento-ss-02]({{ site.baseurl }}/images/magento-ss-02.png)

Crea un nuevo Rol con el nombre *Hoppin-role*.

![magento-ss-04]({{ site.baseurl }}/images/magento-ss-04.png)

Desde *Role Resources*, selecciona acceso *Custom* (o *Personalizado*) y en el árbol de recursos, activa los siguientes permisos:

* Shopping Cart
* Directory

![magento-ss-03]({{ site.baseurl }}/images/magento-ss-03.png)

Recuerda guardar los cambios.

#### Paso 5: Configurar el acceso a través de la API: Crear API Key

Para este paso, será necesario crear un API key para el acceso de Hoppin, que nos tendrás que mandar posteriormente. El valor de esta API key debe ser aleatorio, único y privado. 

Un posible método para generarlo es hacerlo a través de la página https://password.es. Desde está página, seleccionar los siguientes valores:

* Letras
* Letras Mayúsculas
* Números
* Longitude de la contraseña: 24 caracteres

Después, pulsa el botón *Crear contraseña* y copia el valor generado, lo necesitarás en el siguiente paso.

![magento-ss-07]({{ site.baseurl }}/images/magento-ss-07.png)


#### Paso 6: Configurar el acceso a través de la API: Crear Usuario

Pulsa en *System->Web Services->SOAP/XML-RPC - Users* y y crea un nuevo usuario la siguiente información:

* User Name: Hoppin
* First Name: Hoppin
* Last Name: App
* Email: info@hoppin.es
* Current Admin Password: (password de administración de magento)
* New API Key: (introducir el valor generado en el paso anterior)
* API Key Confirmation: (introducir el valor generado en el paso anterior)
* This account is: Active

![magento-ss-05]({{ site.baseurl }}/images/magento-ss-05.png)

Ahora, asigna el Rol creado anteriormente a este usuario y guarda los cambios.

![magento-ss-06]({{ site.baseurl }}/images/magento-ss-06.png)

#### Paso 6 : Configurar el acceso a través de la API: Crear Usuario
