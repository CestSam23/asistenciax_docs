# Usuarios, roles y permisos

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Cuenta con rol principal inicialmente. Prohibido auto-registro público; alta por administrador. Policies/Gates y alcance por coordinación. Evitar desactivar al último administrador; auditar cambios de permisos. Autenticación independiente del expediente de maestro.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/usuarios` | Listar usuarios |
| [ ] | `POST` | `/api/v1/usuarios` | Crear usuario |
| [ ] | `GET` | `/api/v1/usuarios/{id}` | Consultar usuario |
| [ ] | `PATCH` | `/api/v1/usuarios/{id}` | Actualizar usuario |
| [ ] | `POST` | `/api/v1/usuarios/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/usuarios/{id}/desactivar` | Desactivar |
| [ ] | `POST` | `/api/v1/usuarios/{id}/reset-password` | Reset administrativo |
| [ ] | `GET` | `/api/v1/roles` | Roles |
| [ ] | `GET` | `/api/v1/roles/{id}/permisos` | Permisos del rol |
| [ ] | `PUT` | `/api/v1/roles/{id}/permisos` | Configurar permisos (propuesta) |
| [ ] | `GET` | `/api/v1/permisos` | Catálogo permisos |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.


# Rutas despues de revisión

| Método | Endpoint | Función |
|---|---|---|
| GET | `/api/v1/usuarios` | Listar usuarios con filtros y paginación |
| POST | `/api/v1/usuarios` | Crear usuario y enviar invitación |
| GET | `/api/v1/usuarios/{id}` | Consultar usuario |
| PATCH | `/api/v1/usuarios/{id}` | Actualizar usuario |
| POST | `/api/v1/usuarios/{id}/activar` | Reactivar cuenta |
| POST | `/api/v1/usuarios/{id}/desactivar` | Desactivar cuenta |
| POST | `/api/v1/usuarios/{id}/reset-password` | Enviar recuperación de contraseña |
| POST | `/api/v1/usuarios/{id}/reenviar-invitacion` | Reenviar invitación |
| GET | `/api/v1/roles` | Consultar roles |
| GET | `/api/v1/permisos` | Consultar catálogo de permisos |
| GET | `/api/v1/roles/{id}/permisos` | Consultar permisos de un rol |