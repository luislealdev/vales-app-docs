# Distribuidor

## Descripción

El distribuidor es el usuario principal que emite vales a los clientes y gestiona su cartera de clientes. Solo puede gestionar los clientes y vales que están bajo su responsabilidad.

Son responsables de registrar los pagos y entregar al administrador el dinero mensualmente.

## Funciones

- **Crear Vale**: Genera un nuevo vale para un cliente registrado, especificando el monto y el plazo de pago.
- **Registrar Cliente**: Añade nuevos clientes a su base de datos, siempre que estos no estén ya registrados con otro distribuidor.
- **Consultar Vales**: Revisa los vales emitidos y su estado.
- **Modificar y Eliminar Vales**: Puede gestionar los vales creados, si así se decide en el diseño.

## Restricciones

- No puede crear vales para clientes que no están registrados bajo su responsabilidad.
- No puede acceder a vales de otros distribuidores.
