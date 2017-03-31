---
layout: default
title: Prestashop Integration
---

# Integración con tiendas Prestashop 1.6.x
### Compromiso Hoppin: ¡Integración en menos de 30 minutos! :alarm_clock:

En esta guía se describen los pasos para integrar tu tienda con **Hoppin**.


#### Paso 1 : Crear API Key

Necesitamos acceso a tu sistema para leer los productos y poder generar automáticamente los pedidos. Por ello, se hace necesaria la creación de una API Key.

Puedes crear la API Key desde el menú lateral en *Parámetros Avanzados -> Web Services* tal y como se muestra en la imagen:

![presta-ss-01]({{ site.baseurl }}/images/presta-ss-01.png)

Desde esa vista, pulsa el *botón +* para crearla:

![presta-ss-02]({{ site.baseurl }}/images/presta-ss-02.png)

Ahora pulsa en *'Generate'* para que se genere una nueva API Key

![presta-ss-03]({{ site.baseurl }}/images/presta-ss-03.png)

Una vez la haya obtenido, *necesitamos que nos la envíes a info@swipeapp.es*

#### Paso 2 : Crear permisos API Key

Para poder usar la API Key, debemos darle los permisos adecuados. Desde la vista de edición de la API Key, selecciona los siguientes permisos

![presta-ss-04]({{ site.baseurl }}/images/presta-ss-04.png)

* addresses: View (GET) y Add (POST)
* carts: View (GET) y Add (POST)
* countries: View (GET)
* customers: View (GET). Modify (PUT) y Add (POST)
* languages: View (GET)
* orders: View (GET) y Add (POST)

#### Paso 3 : Identificadores

Para poder crear los pedidos, necesitamos que nos facilites algunos identificadores de tu tienda. Apúntalos para enviárnoslos por correo a info@swipeapp.es.

* CountryID (Código para España)

Puedes encontrar este ID pulsando en el menú lateral en *Localización -> Países*

Una vez lo tengas identificado, apunta el valor de la columna ID del país España.

![presta-ss-05]({{ site.baseurl }}/images/presta-ss-05.png)

* LangID

Puedes encontrar este ID pulsando en el menú lateral en *Localización -> Idiomas*

Una vez lo tengas identificado, apunta el que corresponda al idioma Español.

![presta-ss-06]({{ site.baseurl }}/images/presta-ss-06.png)

* CarrierID

De forma similar a los IDs anteriores, puedes encontrar este otro en *Transporte -> Transportistas*

![presta-ss-07]({{ site.baseurl }}/images/presta-ss-07.png)

*NOTA*: Necesitamos que escojas aquí los gastos de envío para los pedidos que se hagana a través de Hoppin y que este sea un valor fijo.

Al igual que antes, apunta el ID correspondiente a este método de envío.


#### Paso 4 : Activar método de pago

Por último, y ya que los pagos os los vamos a procesar nosotros, necesitamos usar un método de pago para reflejarlo en los pedidos. El más adecuado es el denominado *BankWire* (transferencia bancaria).

Si te dirijes a *Módulos y Servicios -> Pago*, podrás activarlo (si es que no lo está ya) fácilmente tal y como se muestra en la figura:

![presta-ss-08]({{ site.baseurl }}/images/presta-ss-08.png)

Una vez activado, asegúrate de ocultarlo en el *checkout* de los usuarios si no quieres que puedan escoger esta opción al comprar directamente en tu tienda web. Para ello pulsa en las siguientes tres opciones:

* Disable on mobiles
* Disable on tablets
* Disable on computers

![presta-ss-07]({{ site.baseurl }}/images/presta-ss-07.png)


