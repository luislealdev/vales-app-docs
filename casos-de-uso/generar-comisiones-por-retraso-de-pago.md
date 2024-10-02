# Generar Comisiones por Retraso en el Pago:

- Descripción: Si el cliente no realiza el pago en la fecha establecida, se le genera una comisión adicional.

- Actores: Cliente, Distribuidor.

- Precondiciones:

* El cliente debe tener un calendario de pagos y un pago vencido.

- Flujo principal:
  - El sistema revisa si ha pasado la fecha límite de pago.
  - Se genera automáticamente una comisión adicional sobre el monto adeudado.
  - Se actualiza el monto total a pagar.

* Excepciones:
  - Si el cliente paga después de la comisión, se le carga automáticamente el nuevo monto con la comisión incluida.
