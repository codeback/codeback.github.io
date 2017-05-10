---
layout: default
title: Prestashop Integration
---

# Integración con tiendas Prestashop 1.6.x
### Compromiso Hoppin: ¡Integración en menos de 30 minutos! :alarm_clock:

En esta guía se describen los pasos para integrar tu tienda con **Hoppin**.  

#### Paso 0: Preparar .htaccess

Este es el paso más técnico de la integración, pero es muy sencillo. Simplemente, accede a tu hosting, encuentra el fichero .htaccess y añade estas líneas:

```
<IfModule mod_rewrite.c>
RewriteEngine on
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
</IfModule>
```

#### Paso 1 : Crear API Key

Necesitamos acceso a tu sistema para leer los productos y poder generar automáticamente los pedidos. Por ello, se hace necesaria la creación de una API Key.

Puedes crear la API Key desde el menú lateral en *Parámetros Avanzados -> Web Services* tal y como se muestra en la imagen:

![presta-ss-01]({{ site.baseurl }}/images/presta-ss-01.png)

Desde esa vista, pulsa el *botón +* para crearla:

![presta-ss-02]({{ site.baseurl }}/images/presta-ss-02.png)

Asegúrate ahora o más adelante de que el botón "Enable Prestashop Webservice" (ver imagen de arriba) en la sección "Configuration" **está activado**.

Ahora pulsa en *'Generate'* para que se genere una nueva API Key

![presta-ss-03]({{ site.baseurl }}/images/presta-ss-03.png)

Una vez la haya obtenido, *necesitamos que nos la envíes a info@hoppin.es*. 


#### Paso 2 : Crear permisos API Key

Para poder usar la API Key, debemos darle los permisos adecuados. Desde la vista de edición de la API Key, selecciona los siguientes permisos

![presta-ss-04]({{ site.baseurl }}/images/presta-ss-04.png)

* **addresses: View (GET) y Add (POST).** Para crear las dirrecciones de los clientes que os llevemos.
* **carriers: View (GET).** Para obtener el identificador del transportista que tendremos que usar.
* **carts: View (GET) y Add (POST).** Para crear el carrito de compra de cada transacción.
* **countries: View (GET).** Para obtener el identificador del país.
* **currencies: View (GET).** Para obtener el identificador de la moneda.
* **customers: View (GET), Modify (PUT) y Add (POST).** Para crear el cliente en vuestro sistema.
* **deliveries: View (GET).** Para obtener los gastos de envío.
* **languages: View (GET).** Para obtener el identificador del idioma.
* **order_states: View (GET).** Para obtener el estado de los pedidos.
* **orders: View (GET) y Add (POST).** Para crear los pedidos en vuestro sistema.  
* **price_ranges: View (GET).** Para calcular los gastos de envío de los pedidos.
* **states: View (GET).** Para calcular los gastos de envío de los pedidos.
* **weight_ranges: View (GET).** Para calcular los gastos de envío de los pedidos.
* **zones: View (GET).** Para calcular los gastos de envío de los pedidos.


#### Paso 3 : Envíos

Para poder crear los pedidos, necesitamos que nos facilites el identificador del transportista que debemos usar. Apúntalo para enviárnoslos por correo a info@hoppin.es.

Puedes encontrarlo en *Transporte -> Transportistas*

![presta-ss-05]({{ site.baseurl }}/images/presta-ss-05.png)

*NOTA*: Necesitamos que escojas aquí los gastos de envío para los pedidos que se hagan a través de Hoppin y que este sea un valor fijo.

Apunta el ID correspondiente a este método de envío.  

También debes enviarnos las reglas de envío que tengas configuradas en ese transportista.

![presta-ss-06]({{ site.baseurl }}/images/presta-ss-06.png)  
  
  
#### Paso 4 : Activar método de pago

Por último, y ya que los pagos os los vamos a procesar nosotros, necesitamos usar un método de pago para reflejarlo en los pedidos. El más adecuado es el denominado *BankWire* (transferencia bancaria).

Si te dirijes a *Módulos y Servicios -> Pago*, podrás activarlo (si es que no lo está ya) fácilmente tal y como se muestra en la figura:

![presta-ss-08]({{ site.baseurl }}/images/presta-ss-08.png)

Una vez activado, asegúrate de ocultarlo en el *checkout* de los usuarios si no quieres que puedan escoger esta opción al comprar directamente en tu tienda web. Para ello pulsa en las siguientes tres opciones:

* Disable on mobiles
* Disable on tablets
* Disable on computers

![presta-ss-09]({{ site.baseurl }}/images/presta-ss-09.png)


