---
layout: default
title: Prestashop Integration
---

# Integración con tiendas Prestashop 1.6.x
### Compromiso Hoppin: ¡Integración en menos de 30 minutos! :alarm_clock:

En esta guía se describen los pasos para integrar tu tienda con **Hoppin**.


#### Paso 1 : Crear API Key

Necesitamos acceso a tu sistema para leer los productos y poder generar automáticamente los pedidos. Por ello, se hace necesaria la creación de una API Key.

Puedes crear la API Key desde ... tal y como se muestra en la imagen

![presta-ss-1]({{ site.baseurl }}/images/presta-ss-1.png)

Una vez la haya obtenido, necesitamos que nos la envíes a info@hoppin.es

#### Paso 2 : Crear permisos API Key

Para poder usar la API Key, debemos darle los permisos adecuados. Son los siguientes:

![presta-ss-2]({{ site.baseurl }}/images/presta-ss-2.png)

#### Paso 3 : Identificadores

Para poder crear los pedidos, necesitamos que nos facilites algunos indicadores de tu tienda:

* CountryID (Código para España)

![presta-ss-3]({{ site.baseurl }}/images/presta-ss-3.png)

* CarrierID

![presta-ss-4]({{ site.baseurl }}/images/presta-ss-4.png)

* LangID

![presta-ss-5]({{ site.baseurl }}/images/presta-ss-5.png)

#### Paso 4 : Activar método de pago

Por último, y ya que los pagos os los vamos a procesar nosotros, necesitamos usar un método de pago para reflejarlo en los pedidos. El más adecuado es el denominado *BankWire* (transferencia bancaria).

Una vez activado, asegúrate de ocultarlo en el *checlout* de los usuarios si no quieres que puedan escoger esta opción al comprar directamente en tu tienda. 

![presta-ss-6]({{ site.baseurl }}/images/presta-ss-6.png)


