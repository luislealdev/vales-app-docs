# Esquema de Entidad-Relación (E-R)

## Entidades

### Usuario

- **idUsuario** (PK): INT, Identificador único del usuario.
- **nombre**: VARCHAR(100), Nombre completo del usuario.
- **correo**: VARCHAR(100), Correo electrónico del usuario.
- **contraseña**: VARCHAR(255), Contraseña encriptada del usuario.
- **rol** (FK): INT, Rol del usuario (relación con la tabla `Rol`).
- **fecha_registro**: DATE, Fecha en la que el usuario se registró.
- **domicilio**: VARCHAR(255), Dirección del usuario.
- **ine**: VARCHAR(18), Identificación INE del cliente.
- **curp**: VARCHAR(18), CURP del cliente.
- **comprobante_domicilio**: VARCHAR(255), Documento que comprueba el domicilio.

### Rol

- **idRol** (PK): INT, Identificador único del rol.
- **nombreRol**: VARCHAR(50), Nombre del rol (Distribuidor, Cliente, Administrador).

### Vale

- **idVale** (PK): INT, Identificador único del vale.
- **monto**: DECIMAL(10, 2), Valor monetario total del vale.
- **fecha_creacion**: DATE, Fecha en que el vale fue creado.
- **codigo**: VARCHAR(255), Código único del vale (UUID).
- **estado**: VARCHAR(50), Estado del vale (activo, usado, vencido, etc.).
- **idDistribuidor** (FK): INT, Identificador del distribuidor que generó el vale.
- **idCliente** (FK): INT, Identificador del cliente al que pertenece el vale.

### Pago

- **idPago** (PK): INT, Identificador único del pago.
- **monto_pagado**: DECIMAL(10, 2), Monto pagado por el cliente.
- **fecha_pago**: DATE, Fecha en la que se realizó el pago.
- **idVale** (FK): INT, Identificador del vale al que corresponde el pago.
- **idDistribuidor** (FK): INT, Identificador del distribuidor que registró el pago.
- **estado**: VARCHAR(50), Estado del pago (completo, parcial, etc.).
- **fecha_vencimiento**: DATE, Fecha de vencimiento del pago.
- **tolerancia**: INT, Días de tolerancia antes de aplicar la comisión.
- **comision**: DECIMAL(5, 2), Porcentaje de comisión aplicada por demora.

### HistorialNotificaciones

- **idNotificacion** (PK): INT, Identificador único de la notificación.
- **mensaje**: TEXT, Mensaje de la notificación.
- **fecha_envio**: DATE, Fecha en la que se envió la notificación.
- **idUsuario** (FK): INT, Identificador del usuario que recibe la notificación.
- **tipoNotificacion**: VARCHAR(50), Tipo de notificación (pago pendiente, comisión aplicada, etc.).

## Relaciones

- `Usuario` (distribuidor) tiene muchos `Vale`.
- `Vale` tiene muchos `Pago`.
- `Pago` es registrado por un `Usuario` (distribuidor) y está vinculado a un `Vale`.
- `HistorialNotificaciones` está vinculado a un `Usuario` (cliente o distribuidor).
