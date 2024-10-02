# Consulta de Ventas y Pagos

- Actor: Distribuidor, Administrador
- Descripción: Los distribuidores y administradores consultan el historial de ventas y pagos relacionados con los vales.
- Flujo principal:

  1. El distribuidor o administrador accede al sistema y selecciona "Consultar Ventas y Pagos".
  2. El sistema muestra una lista de ventas y pagos realizados.
  3. El distribuidor o administrador filtra la consulta por cliente, fecha, sucursal o estado de pago.
  4. El sistema muestra los resultados filtrados.

- Excepciones:
  - Si no hay ventas o pagos registrados, el sistema debe mostrar un mensaje indicando que no hay registros.
  - Si el distribuidor intenta acceder a ventas o pagos de otro distribuidor, el sistema debe bloquear el acceso y notificar la falta de autorización.
