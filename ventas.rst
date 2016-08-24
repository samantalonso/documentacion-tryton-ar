Circuito Ventas
===================

En **Tryton** el concepto *Venta* no se limita únicamente la venta en sí, sino
que engloba todo el proceso que se llevará a cabo: desde la presentación de un
presupuesto hasta la formalización del pedido. Todo ello se gestiona en un
mismo documento que irá cambiando de estado según vaya avanzando el proceso de
la venta. En primer lugar veremos como crear una venta nueva y posteriormente
profundizaremos en los distintos estados en los que podemos encontrar la venta.


Configuración
-------------

En Ventas / Configuración podemos definir los valores por defecto para los campos Método de facturación y Método de envío. 
Para el campo Método de facturación podremos elegir entre:

* Manual: No se generará ninguna factura de forma automática y tendremos que generar nosotros la factura de forma manual. 
* Al procesar el pedido: Una vez la venta cambia a estado En proceso se generará un factura con todas las líneas del pedido de venta en estado borrador.
* Al enviar: Se generará una factura cada vez que se realice el envío de un albarán. Si el albarán no contiene todos los productos de la venta, sólo se facturarán aquellos productos que hayan sido enviados.

En el campo Método de envío podremos elegir entre:

* Manual: No se generará ningún albarán de forma automática y tendremos que generar nosotros el movimiento de stock.
* Al procesar el pedido: Una vez cambie el estado de la venta a En proceso se generará un albarán con todos los movimientos de existencias necesarios.
* Al pagar la factura: Se generarán los albaranes de aquellos productos que en sus respectivas facturas hayan sido pagados.

Ventas
======

En esta sección se armarán las facturas, cumpliendo siempre con el flujo de facturación, que arranca desde el borrador hasta la factura en sí misma.
Podríamos representarlo así:

 /Borrador > Presupuesto > Confirmada > En proceso > Realizada/
                          > Cancelada/



Crear una nueva venta
---------------------

Al acceder a ventas se nos abrirá una pestaña con un listado de las ventas que hemos ido introduciendo con anterioridad clasificadas según el estado en el que se encuentran (*Borrador*, *Presupuesto*, *Confirmado*, *En proceso*).
Además, también podremos ver un listado con todas las ventas realizadas, independientemente de su estado. Haciendo doble clic sobre cualquier cualquier venta del listado accederemos a su información concreta y detallada. Si lo que queremos es crear una venta nueva deberemos hacer click sobre el icono *Nuevo* y se nos abrirá el formulario de edición con los campos que deberemos rellenar para crear la venta.


La venta está compuesta por una parte en la que se define el cliente con sus datos (Cabecera), y otra compuesta por varias pestañas que contendrán información concreta sobre la venta en sí. En la cabecera, una vez indiquemos el Tercero se rellenarán automáticamente los campos Dirección de facturación y Dirección de envío con la información que tengamos en la ficha del Tercero, pudiéndolos modificar si lo deseamos.

En la pestaña Venta podremos indicar la Fecha de venta, el Almacén desde donde se realiza la venta, la Moneda y el Plazo de pago. Estos dos últimos campos también se rellenarán automáticamente con la información que tengamos del Tercero en su ficha.

En el campo Tipo de pago podremos relacionar la venta con un tipo de pago acordado con el tercero. El tipo de pago se traspasará del pedido de venta a la factura cuando esta se genere.

En Tarifa también podremos indicar la tarifa de venta que se aplicará al pedido de venta en caso de que queramos que se le aplique alguna.

Además, para calcular el precio del coste de envío, deberemos indicar el Portes que realizará la entrega y el Método de coste envío en la pestaña Información adicional. En el momento de seleccionar un Portes también se generará una nueva línea en el pedido de venta con el coste y producto del envío. Cada vez que cambie una línea (ya sea el producto, precio o cantidad) esta línea se generará de nuevo. En el caso que sea un pedido que ya se haya guardado, se eliminará la línea creando una de nueva.

Por último, tendremos que rellenar el campo Líneas con la información de los productos que serán objeto de la venta, creando tantas líneas como productos distintos vayamos a vender o presupuestar. Para generar una línea clicaremos en el icono Nuevo del campo Líneas y se nos abrirá un ventana emergente con los siguientes campos:

* Tipo: Mediante este campo podremos definir distintos tipos de línea. El valor por defecto es Línea, si mantenemos este Tipo deberemos rellenar también los campos que siguen a este en la explicación. Los otros valores son Comentario, Subtotal y Título que se utilizan para añadir líneas extras que aparecerán en el informe permitiendo de esta forma una personalización más sencilla. Estos últimos tres tipos se componen únicamente de los campos Descripción y Secuencia.
* Producto: Aquí seleccionaremos el producto que queremos vender o presupuestar. Establecer un producto es opcional, de todos modos, si queremos que estos productos estén en los albaranes y se hagan los correspondientes movimientos de stock, deberemos seleccionar forzosamente un producto que no sea de tipo servicio.
* Descripción: En este campo reflejaremos aquello que aparecerá como descripción de la línea en la venta. Si indicamos previamente el Producto, este campo se rellenará automáticamente con el nombre del producto, aunque podremos modificarlo.
* Cantidad y Unidad: Indicaremos la cantidad y la unidad de medida del producto que estamos introduciendo.
* Precio unidad: Cuando indiquemos (o se nos rellene el campo con la información introducida en la ficha del producto) el precio por unidad al que vendemos el producto, se nos rellenará de forma automática el campo Importe con el total de la línea.
* Impuestos: Si tenemos configurados los productos con el impuesto que les corresponde, este campo se nos rellenará automáticamente con la información indicada en el producto, si no, deberemos indicar qué impuesto gravará la línea de la venta.

