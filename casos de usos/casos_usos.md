### Caso de uso 1: Registrar Cliente

- Actor principal: Administrador
- Requerimientos: RF1.1
- Precondiciones:
    - El usuario ha iniciado sesión en el sistema.

#### Flujo principal

    1.El usuario ingresa los datos del cliente (nombre, apellido, DNI, teléfono, email, dirección).

    2.El sistema verifica los datos ingresados por el usuario.

    3.El sistema registra el nuevo cliente en la base de datos.

#### Flujo alternativo

    2.a Algún dato obligatorio está vacío → Vuelve al paso 1.

    2.b Formato inválido en algún campo (DNI, email, etc.) → Vuelve al paso 1.

    2.c El cliente ya existe en el sistema → Vuelve al paso 1.

#### Postcondición:

    - El cliente queda guardado y registrado.

### Caso de uso 2: Modificar Cliente

Actor principal: Administrador
Requerimientos: RF1.2

Precondiciones:

   - El usuario ha iniciado sesión en el sistema.

   - El cliente a modificar debe existir.

#### Flujo principal

    1.El usuario selecciona la opción “Modificar Cliente”.

    2.El sistema solicita un criterio de búsqueda.

    3.El usuario ingresa el criterio  id_cliente.

    4.El sistema muestra la información actual del cliente.

    5.El usuario modifica los datos necesarios.

    6.El sistema valida los datos modificados.


#### Flujo alternativo

    3.a Cliente no encontrado. Vuelve al paso 2.

    6.a Algún dato modificado no cumple el formato. Vuelve al paso 5.

#### Postcondición:

- La información del cliente queda actualizada.

### Caso de uso 3: Consultar Cliente

- Actor principal: Administrador  
- Requerimientos: RF1.3  

Precondiciones:

- El usuario ha iniciado sesión en el sistema.
- Debe existir al menos un cliente registrado.

#### Flujo principal

    1. El usuario selecciona la opción “Consultar Cliente”.
    2. El sistema solicita un criterio de búsqueda.
    3. El usuario ingresa el criterio id_cliente.
    4. El sistema muestra la información completa del cliente.

#### Flujo alternativo

    3.a Cliente no encontrado. Vuelve al paso 2.

##### Postcondición:

- Se visualiza la información completa del cliente (sin modificaciones).