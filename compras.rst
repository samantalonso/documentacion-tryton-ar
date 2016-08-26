Compras
========

Gestión de Compras
------------------

En Tryton el concepto de Compra no se limita únicamente la compra en sí, sino que engloba todo el proceso que se llevará a cabo: desde que nos presentan un presupuesto de compra hasta la formalización del pedido. Todo ello se gestiona en un mismo documento que irá cambiando de estado según vaya avanzando el proceso de compra. En primer lugar veremos como crear una compra nueva y posteriormente profundizaremos en los distintos estados en los que podemos encontrar la compra.

Crear una nueva compra
----------------------

Para crear una nueva compra deberemos acceder a Compras / Compras y se nos abrirá una pestaña con un listado de las compras introducidas con anterioridad, clasificadas según el estado en el que se encuentran (Borrador, Presupuesto, Confirmado, En proceso). Además, también podremos ver un listado con todas las compras realizadas, independientemente de su estado, desde la subpestaña Todo (más adelante, en Flujo de compras, veremos más detenidamente cada uno de los estados). Haciendo doble clic sobre cualquier compra del listado accederemos a su información concreta y detallada. Si lo que queremos es crear una compra nueva deberemos clicar sobre el icono Nuevo y se nos abrirá el formulario de edición con los campos que deberemos rellenar para crear la compra.




La compra está compuesta por una parte en la que se define el proveedor con sus datos (Cabecera), y otra compuesta por varias pestañas que contendrán información concreta sobre la compra en sí. En la cabecera, una vez indiquemos el Tercero se rellenará automáticamente el campo Dirección de facturación con la información que tengamos en la ficha del Tercero, pudiéndola modificar si lo deseamos.

En la pestaña Compra podremos indicar la Fecha de compra, el Almacén que recibirá la compra, la Moneda y el Plazo de pago. Estos dos últimos campos también se rellenarán automáticamente con la información que tengamos del Tercero en su ficha. Por último, tendremos que rellenar el campo Líneas con la información de los productos que serán objeto de la compra, creando tantas líneas como productos distintos vayamos a comprar. Para generar una línea clicaremos en el icono Nuevo del campo Líneas y se nos abrirá un ventana emergente con los siguientes campos:

* Tipo: Mediante este campo podremos definir distintos tipos de línea. El valor por defecto es Línea, si mantenemos este Tipo deberemos rellenar también los campos que siguen a este en la explicación. Los otros valores son Comentario, Subtotal y Título que se utilizan para añadir líneas extras que aparecerán en el informe, permitiendo de esta forma una personalización más sencilla. Estos últimos tres tipos se componen únicamente de los campos Descripción y Secuencia.
* Producto: Aquí seleccionaremos el producto que vayamos a comprar. Establecer un producto es opcional, de todos modos, si queremos generar albaranes de proveedor y que se hagan los correspondientes movimientos de stock, deberemos seleccionar forzosamente un producto que no sea de tipo servicio.
* Descripción: En este campo reflejaremos aquello que aparecerá como descripción de la línea en la compra. Si indicamos previamente el Producto, este campo se rellenará automáticamente con el nombre del producto, aunque podremos modificarlo.
* Cantidad y Unidad: Indicaremos la cantidad y la unidad de medida del producto que estamos introduciendo.
* Precio unidad: Cuando indiquemos (o se nos rellene el campo con la información introducida en la ficha del producto) el precio por unidad al que vendemos el producto, se nos rellenará de forma automática el campo Importe con el importe total,teniendo en cuenta la Cantidad que hemos introducido.
* Impuestos: Si tenemos configurados los productos con el impuesto que les corresponde, este campo se nos rellenará automáticamente con la información indicada en el producto, si no, deberemos indicar qué impuesto gravará la línea de la compra.
Si accedemos a la pestaña Información adicional podremos indicar en el campo Método de facturación en qué punto de la compra queremos que se genere la factura. Para ello podremos elegir entre:

* Manual: No se generará ninguna factura de forma automática y tendremos que generar nosotros la factura de forma manual. (Cómo generar una factura manualmente).
* Basado en el pedido: Una vez la compra cambia a estado En proceso se generará un factura con todas las líneas del pedido de compra en estado borrador.
* Basado en el envío: Se generará una factura cada vez que se haga efectiva la recepción de la mercancía. Si el albarán no contiene todos los productos de la compra, sólo se facturarán aquellos productos que hayan sido recibidos.
Como se indica en el apartado Configuración, podemos configurar el método de facturación por defecto que se mostrarán en las compras.

Desde las pestañas facturas y albaranes podremos acceder a la información sobre las recepciones y facturación de la compra. Una vez se generen los albaranes o facturas, nos aparecerán en sus respectivas pestañas y podremos acceder a la información concreta de cada documento. En Estado factura y Estado envío se indica en qué estados nos podemos encontrar estos dos documentos.
