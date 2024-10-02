# Registrar Cliente

   - Actor: Distribuidor
   - Descripción: El distribuidor registra a un nuevo cliente en el sistema.
   - Flujo principal:

   1. El distribuidor ingresa los datos del cliente (nombre, domicilio, INE, CURP, comprobante de domicilio).
   2. El sistema valida que el cliente no esté registrado por otro distribuidor.
   3. El sistema guarda el registro del cliente y lo asocia al distribuidor.
   4. El distribuidor recibe una notificación de confirmación.

   - Excepciones:
     - Si el cliente ya está registrado por otro distribuidor, el sistema debe rechazar el registro.
     - Si se omite algún dato obligatorio, el sistema no debe permitir continuar hasta que se ingrese correctamente.
