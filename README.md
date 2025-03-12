# Optimización de una Base de Datos de Ventas

Una tienda en línea ha notado que su sistema de gestión de pedidos se ha vuelto lento,
especialmente al consultar el historial de compras de los clientes y al actualizar el inventario
después de cada venta. Los informes de ventas tardan demasiado en generarse, afectando la
toma de decisiones en tiempo real.

Los problemas identificados incluyen:

1. Consultas lentas al buscar pedidos por cliente.
2. Bloqueos en la base de datos cuando múltiples transacciones intentan actualizar el
    inventario.
3. Ausencia de índices adecuados en tablas de gran tamaño.

## 1. Objetivo:

1. Optimizar las consultas y mejorar el rendimiento del sistema.
2. Reducir bloqueos y mejorar la concurrencia en operaciones críticas.
3. Aplicar técnicas avanzadas como índices, transacciones eficientes y stored procedures.

## 2. Tablas del Sistema:

### Clientes: Almacena datos de los clientes

ClienteID,
Nombre,
CorreoElectronico,
Telefono,
FechaRegistro

### Productos: Almacena productos vendidos
ProductoID
NombreProducto
Descripcion
Precio
Stock

### Pedidos: Registra las Ventasr realizadas.

PedidoID,
ClienteID,
FechaPedido,
Estado,
Total

### DetalleVenta: Guarda los productos vendidos en cada pedido.

DetalleID,
PedidoID,
ProductoID,
Cantidad,
PrecioUnitario

### Pagos: Registra los pagos de cada pedido.

PagoID,
PedidoID,
Monto,
MetodoPago,
FechaPago

## 3. Tareas mínimas:

- Creación de la DB
- Índices para Acelerar Consultas
- Transacción para Actualizar Stock y Registrar Venta
- Stored Procedure para Consultar Ventas por Cliente
- Describe el proceso de las optimizaciones y conclusiones.

