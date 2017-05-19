---
layout: default
title: Magento Integration
---

# Integración con tiendas Magento 1.9.x
### Compromiso Hoppin: ¡Integración en menos de 30 minutos! :alarm_clock:

En esta guía se describen los pasos para integrar tu tienda con **Hoppin**.


#### Paso 1 : Subir el módulo Hoppin

Descarga el módulo aquí: [Descargar Módulo]({{ site.url }}/download/hoppin-magento.zip)

Sube el módulo al directorio raíz de tu instalación de Magento y descomprímelo. Este módulo creará un nuevo método de pago (llamado Hoppin) y hará que no se muestre en el *checkout* a los usuarios que compren de modo convencional en la web de la tienda.


#### Paso 2 : Medida de precaución (Just in case)

* Crea una copia de seguridad desde *System->Tools->Backup*
* Deshabilita las compilaciones en *System->Tools->Compilations*
* Limpia la caché en *System -> Cache Management*

Ahora, sal de la sesión de administrador de Magento y accede de nuevo.


#### Paso 3 : Configurar el módulo

Dirígete a *System->Configuration->Payment Methods*, encuentra el nuevo método de pago Hoppin y seleccionar el **New order status** que desees para los pedios que se generen desde Hoppin.

![magento-ss-3]({{ site.baseurl }}/images/magento-ss-3.png)
