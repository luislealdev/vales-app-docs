# Principales Entidades del Modelo de Dominio:

## Cliente:

    * Atributos:
        - idCliente: Identificador único del cliente.
        - nombre: Nombre completo del cliente.
        - domicilio: Dirección física del cliente.
        - INE: Identificación oficial del cliente (INE).
        - CURP: Clave única del cliente en México.
        - comprobanteDomicilio: Documento que verifica la dirección del cliente.
        - deudaTotal: Total de deuda acumulada.
        - historialPagos: Lista de pagos que el cliente ha realizado.
        - fechaUltimoPago: Fecha del último pago registrado.

    * Relaciones:
        - Un cliente puede tener varios vales asociados.

## Distribuidor:

    * Atributos:
        - idDistribuidor: Identificador único del distribuidor.
        - nombre: Nombre del distribuidor.
        - clientes: Lista de clientes que el distribuidor tiene asignados.
        - valesEmitidos: Vales que ha emitido a los clientes.
        - historialPagosRecibidos: Lista de pagos que ha registrado de los clientes.
        - fondosMensuales: Total de dinero que el distribuidor debe entregar al administrador al final del mes.

    * Relaciones:
        - Un distribuidor puede emitir varios vales.
        - Un distribuidor tiene varios clientes asignados.

## Administrador:

    * Atributos:
        - idAdministrador: Identificador único del administrador.
        - nombre: Nombre del administrador.
        - distribuidores: Lista de distribuidores que administra.
        - historialPagosRecibidos: Lista de pagos totales recibidos de los distribuidores.

    * Relaciones:
        - Un administrador puede gestionar varios distribuidores.
        - Recibe los fondos de los distribuidores.

## Vale:

    * Atributos:
        - idVale: Identificador único del vale (UUID).
        - monto: Monto total del vale.
        - montoRestante: Monto que queda por pagar.
        - cliente: Cliente al que fue otorgado.
        - distribuidor: Distribuidor que emitió el vale.
        - fechaEmision: Fecha en la que fue emitido el vale.
        - fechaVencimiento: Fecha límite para el uso o canje del vale.
        - estatus: Estado actual del vale (Activo, Pagado, Vencido, etc.).

    *Relaciones:
        - Un vale pertenece a un cliente y a un distribuidor.
        - Está asociado a pagos realizados por el cliente.

## Pago:

    * Atributos:
        - idPago: Identificador único del pago.
        - montoPago: Monto del pago realizado.
        - fechaPago: Fecha en la que se realizó el pago.
        - formaPago: Forma en que se hizo el pago (efectivo o transferencia).
        - cliente: Cliente que realizó el pago.
        - distribuidor: Distribuidor que registró el pago.
        - vale: Vale asociado al pago.

    *Relaciones:
        - Un pago está asociado a un cliente, un vale y un distribuidor.

## Notificación:

    * Atributos:
        - idNotificacion: Identificador único de la notificación.
        - tipo: Tipo de notificación (Recordatorio de pago, Advertencia de multa, etc.).
        - fechaEnvio: Fecha en la que se envió la notificación.
        - estado: Estado de la notificación (Enviada, Pendiente).
        - cliente: Cliente que recibe la notificación.

    * Relaciones:
        - Cada notificación está asociada a un cliente.

    * Relaciones Clave:
        1. Cliente - Vale: Un cliente puede tener varios vales asociados. Cada vale puede estar relacionado con diferentes pagos y deudas.
        2. Distribuidor - Cliente: Un distribuidor puede tener varios clientes registrados, y es responsable de gestionar los vales emitidos y los pagos recibidos.
        3. Administrador - Distribuidor: Un administrador tiene acceso a los registros de cada distribuidor, y cada distribuidor debe reportar sus fondos al administrador al final del mes.
        4. Pago - Vale - Cliente - Distribuidor: Cada pago realizado por un cliente es registrado por un distribuidor, y está vinculado a un vale.
