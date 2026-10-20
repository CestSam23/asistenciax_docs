# Roles
El sistema cuneta con 4 roles.

**Administrador** (Pastor Hugo e Isa, Mitzi, It)
**Coordinador**
**Maestros**
**Apoyo** (Antorchas, audio, video, etc)

## RBAC

El sistema funcionara bajo un modelo de desarrollo RBAC.
En primera instancia, contaremos con los siguientes permisos para roles:
| Funcionalidad | Admin | Coordinador | Maestro | Apoyo |
|---|---|---|---|---|
| Consultar usuarios del sistema | Sí | No | No | No |
| Crear usuarios | Sí | No | No | No |
| Modificar usuarios | Sí | No | No | No |
| Activar y desactivar cuentas | Sí | No | No | No |
| Asignar roles | Sí | No | No | No |
| Consultar maestros de su coordinación | Sí, todas | Sí | No | No |
| Consultar asistencias | Todas | Su coordinación | Según operación | Por definir |
| Registrar asistencias | Sí | Sí | Sí | Por definir |
| Consultar reportes | Generales | Su coordinación | Por definir | Por definir |
| Modificar permisos de roles | No, solo backend | No | No | No |


Administrador
Los cuatro administradores tendrán autoridad para gestionar las cuentas del sistema.

Podrán crear usuarios, asignar cualquiera de los cuatro roles y activar o desactivar cuentas.

Mantendremos las protecciones contra la pérdida del último administrador activo.
Coordinador
Podrá supervisar las actividades y consultar información operativa correspondiente a su coordinación.

No podrá crear usuarios, modificar sus cuentas, cambiar roles ni desactivarlos.

Por ejemplo, el coordinador de Orugas podrá consultar los maestros de Orugas, pero no tendrá acceso administrativo a los maestros de Leones.
Maestro
Tendrá acceso a las funcionalidades necesarias para atender a los niños y registrar asistencias.

No tendrá permisos administrativos sobre usuarios.
Apoyo
Tendrá permisos operativos limitados, que definiremos según las funcionalidades que realmente necesite.

