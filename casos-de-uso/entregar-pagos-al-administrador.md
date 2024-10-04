# Entrega de Pagos al Administrador (Distribuidor)

- Descripción: El distribuidor debe entregar al administrador todos los fondos recolectados de los pagos de sus clientes al final de cada mes.

- Actor: Distribuidor

- Precondiciones

  - El distribuidor ha registrado pagos de los clientes durante el mes.

- Flujo principal

  1. Al final del mes, el distribuidor genera un resumen de todos los pagos recibidos en la aplicación.
  2. El sistema calcula el monto total que debe entregarse al administrador.
  3. El distribuidor realiza la entrega física o virtual del dinero al administrador.
  4. El sistema actualiza el estado de los pagos entregados.

- Postcondiciones

  - Los pagos quedan registrados como entregados al administrador.
  - Se genera un recibo de confirmación para el distribuidor y el administrador.

- Exepciones
  - Si el distribuidor intenta registrar un monto incorrecto o no coincide con los pagos registrados, el sistema muestra un error y solicita revisar la información.
