# Realizar Pago de Vale

- Descripción: El cliente realiza un pago parcial o total correspondiente al monto de un vale.

- Actores: Cliente, Distribuidor.

- Precondiciones:

  - El vale debe estar vigente y tener montos pendientes.
  - El cliente debe estar registrado y tener un calendario de pagos asociado al vale.

  * Flujo principal:

    1. El cliente elige el monto que desea pagar (puede ser total, parcial o adelantado).
    2. El distribuidor confirma el pago.
    3. Se actualiza el estado del pago en el sistema.
    4. Si el pago cubre más de un mes o adelanta pagos futuros, se ajusta el calendario de pagos.

- Excepciones:
  - Si el monto es menor al esperado (e.g., un pago incompleto de la mensualidad), se debe notificar que el saldo queda pendiente.
  - Si hay un problema técnico durante el pago, el sistema debe anular el proceso y notificar al distribuidor.
