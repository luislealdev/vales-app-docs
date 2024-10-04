# Consultar pagos y deudas (Cliente)

- Descripción: El cliente puede ver el estado de sus pagos y deudas, pero no tiene la capacidad de realizar pagos directamente en la aplicación.

- Actor: Cliente

- Precondiciones:

  - El cliente debe tener al menos un vale activo.

- Flujo principal:

  1. El cliente accede a su perfil y selecciona la opción para ver pagos y deudas.
  2. El sistema muestra el historial de pagos, el monto adeudado y las fechas de vencimiento de las mensualidades.
  3. El cliente revisa el detalle de cada pago y el estado de sus deudas.

- Postcondiciones:

  - El cliente puede visualizar su deuda, pero no realizar pagos desde la aplicación.

- Excepciones:
  - Si no hay conexión a la base de datos, el sistema muestra un error e invita a intentar más tarde.
