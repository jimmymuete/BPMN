# Introducción

La zapatería Paso Firme es un establecimiento dedicado a la venta, inventario y gestión de productos de calzado. Este documento de dominio describe de manera estructurada los principales elementos, procesos y reglas que definen el funcionamiento del negocio, complementado con un análisis BPMN (Business Process Model and Notation). El objetivo es representar el flujo del negocio, sus actores, actividades, recursos y restricciones, presentado en formato Markdown (MD) y equivalente a aproximadamente 5 páginas.

#  2. Descripción General del Dominio

La zapatería Paso Firme opera de forma presencial y semidigital. Su objetivo principal es ofrecer calzado de diferentes tipos (deportivo, casual, formal, infantil y especializado) a clientes finales. El dominio incluye los procesos de atención, ventas, facturación, control de inventario, abastecimiento y gestión postventa.

## 2.1 Actores Principales

Cliente: Persona que compra calzado o consulta disponibilidad de productos.

Vendedor: Atiende, asesora, realiza registro de ventas y procesa pagos.

Administrador: Supervisa operaciones, controla inventario y proveedores.

Proveedor: Empresa o persona que suministra el calzado.

## 2.2 Objetos del Dominio

Producto (Calzado): Identificado por código, referencia, talla, color, precio y tipo.

Inventario: Registro de existencias de cada producto.

Factura: Documento que respalda la venta.

Pedido: Solicitud de producto a proveedores.

Pago: Método y confirmación de compra del cliente.

# 3. Procesos Principales del Negocio

A continuación se presentan los procesos modelados en un BPMN conceptual y detallado.

## 3.1 Proceso: Atención y Venta al Cliente

El cliente ingresa a la tienda.

El vendedor lo recibe y consulta su necesidad.

Se realiza búsqueda del calzado solicitado.

Se verifica disponibilidad en inventario.

Si hay disponibilidad, se muestra el producto.

El cliente se prueba el calzado.

Si decide comprar, el vendedor registra la venta.

Se genera la factura.

Se realiza el pago.

Se entrega el producto.

## 3.2 Proceso: Gestión de Inventario

Registrar nuevo calzado recibido.

Actualizar cantidades disponibles.

Verificar niveles mínimos de inventario.

Generar alerta de reposición.

Elaborar pedido al proveedor.

## 3.3 Proceso: Abastecimiento con Proveedor

Se elabora el pedido.

Se envía al proveedor.

El proveedor confirma disponibilidad.

Se recibe la mercancía.

Se actualiza inventario.

Se verifica factura del proveedor.

# 4. Diagrama BPMN (Descripción en Texto)

A falta de diagrama visual, se describe el BPMN de manera estructurada.

## 4.1 Pool y Lanes

Pool: Zapatería Paso Firme

Lane: Cliente

Lane: Vendedor

Lane: Administrador

Lane: Proveedor

## 4.2 Flujo del Proceso Principal (Venta)

Start Event: Cliente entra a la tienda.

Task (Vendedor): Saludar y asesorar.

Task (Vendedor): Consultar inventario.

Gateway: ¿Producto disponible?

Sí: Mostrar producto.

No: Informar al cliente, ofrecer alternativas → End Event.

Task (Cliente): Probar calzado.

Gateway: ¿Compra confirmada?

Sí: Continuar.

No: Agradecer y finalizar → End Event.

Task (Vendedor): Registrar venta.

Task (Sistema): Generar factura.

Task (Cliente): Realizar pago.

End Event: Entregar producto.

# 5. Reglas del Dominio

No se puede registrar una venta sin inventario disponible.

Todo producto debe tener una referencia única.

Las facturas deben incluir fecha, identificación del cliente y detalle de productos.

Los niveles mínimos de inventario deben mantenerse para evitar agotados.

Los pedidos a proveedores deben ser autorizados por el administrador.

El sistema debe registrar cada entrada y salida de productos.

# 6. Casos de Uso del Sistema
# 6.1 Caso de Uso: Registrar Venta

Actor: Vendedor

Flujo Principal: Seleccionar producto → Registrar cliente → Generar factura → Procesar pago → Guardar registro.

# 6.2 Caso de Uso: Actualizar Inventario

Actor: Administrador

Flujo Principal: Ingresar producto → Registrar cantidades → Verificar stock.

# 6.3 Caso de Uso: Realizar Pedido a Proveedor

Actor: Administrador

Flujo Principal: Identificar productos bajos → Crear pedido → Enviar → Recibir mercancía.
