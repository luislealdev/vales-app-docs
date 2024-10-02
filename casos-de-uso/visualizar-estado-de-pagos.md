# Visualizar Estado de Pagos:

- Descripción: El cliente y el distribuidor pueden visualizar el estado de los pagos asociados a un vale.

- Actores: Cliente, Distribuidor, Administrador.

* Precondiciones:

  - El cliente debe tener un vale activo con pagos pendientes.

* Flujo principal:

  1. El cliente accede a la sección de "Pagos".
  2. El sistema muestra el estado de cada mensualidad, junto con los pagos realizados, pagos pendientes y comisiones.
  3. El cliente puede ver un historial de pagos y adelantos, y el distribuidor puede ver un resumen de todos sus clientes.

* Excepciones:
  - Si el cliente no tiene ningún vale activo, se muestra un mensaje indicando que no hay pagos pendientes.
