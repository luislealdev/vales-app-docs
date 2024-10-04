# Realizar Pago de Vale

- Descripción: El distribuidor es el encargado de registrar los pagos recibidos por el cliente, ya sea en efectivo o por transferencia. Una vez registrado el pago, el distribuidor tiene la responsabilidad de entregar los fondos al administrador al final del mes.

- Actores: Distribuidor.

- Precondiciones:

  - El cliente debe haber entregado el pago al distribuidor.
  - El distribuidor tiene acceso a la aplicación para registrar el pago.

  * Flujo principal:

    1. El distribuidor selecciona al cliente que realizó el pago y el vale correspondiente.
    2. El sistema muestra el monto adeudado y las mensualidades pendientes.
    3. El distribuidor ingresa el monto recibido.
    4. El sistema registra el pago, actualiza el saldo del cliente y muestra la deuda restante.
    5. El distribuidor entrega los fondos al administrador al final del mes.
  
- Postcondiciones
  - El pago del cliente queda registrado en el sistema.
  - El sistema actualiza el historial de pagos del cliente.

- Excepciones:
  - Si el distribuidor intenta registrar un monto mayor al adeudado, el sistema lo rechaza.
  - Si hay un problema técnico durante el pago, el sistema debe anular el proceso y notificar al distribuidor.
