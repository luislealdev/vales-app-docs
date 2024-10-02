# Crear Vale

   - Actor: Distribuidor
   - Descripción: El distribuidor selecciona un cliente y genera un vale con un monto específico y el número de meses para pagarlo.
   - Flujo principal:

     1. El distribuidor selecciona a un cliente registrado.
     3. Ingresa el monto del vale y la cantidad de meses para pagar.
     4. El sistema genera un código único (UUID) para el vale.
     5. Se registra la fecha de vencimiento y las mensualidades.
     6. El sistema guarda el vale y notifica al distribuidor.

   - Excepciones:
     - Si el cliente no está registrado, el distribuidor deberá registrar al cliente antes de poder crear el vale.
     - Si se genera un código duplicado, el sistema debe crear uno nuevo (UUID) automáticamente.
     - Si ocurre un error técnico durante la creación, el sistema debe cancelar la transacción e informar al distribuidor.
