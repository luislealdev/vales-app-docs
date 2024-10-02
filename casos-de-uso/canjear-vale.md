2. Canjear Vale

- Actor: Sucursal, Cliente
- Descripción: El cliente presenta un vale en la sucursal, donde se valida el código y se canjea el monto correspondiente.
- Flujo principal:

  1. El cliente presenta su vale en la sucursal.
  2. La sucursal accede al sistema y selecciona "Canjear Vale".
  3. Ingresa el código del vale.
  4. El sistema valida el código del vale.
  5. Si el monto del producto es menos o igual al vale, la transacción se completa.
  6. Si el monto del producto es mayor al valor del vale, se rechaza la transacción y se sugiere contactar al distribuidor.
  7. El sistema registra la transacción y actualiza el estado del vale.

- Excepciones:
  - Si el cliente intenta canjear más del valor del vale, la transacción debe ser rechazada.
  - Si el vale no existe o ya ha sido canjeado, el sistema debe notificar el error y sugerir al cliente contactar al distribuidor.
  - Si hay problemas de conexión, el sistema no debe registrar la transacción hasta que se reestablezca la conexión.
