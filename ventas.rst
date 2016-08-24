Ventas
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
------

En esta sección se armarán
