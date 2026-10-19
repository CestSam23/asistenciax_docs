# Autenticación

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Sesiones Sanctum SPA mediante cookies, CSRF y expiración. Sin registro público. Solo personal de iglesia; tutores no inician sesión. Login por correo y contraseña, desactivación bloquea acceso; registro de usuarios es administrativo.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/sanctum/csrf-cookie` | Obtener cookie CSRF |
| [ ] | `POST` | `/api/v1/auth/login` | Iniciar sesión |
| [ ] | `POST` | `/api/v1/auth/logout` | Cerrar sesión |
| [ ] | `GET` | `/api/v1/auth/me` | Usuario y permisos |
| [ ] | `POST` | `/api/v1/auth/change-password` | Cambiar contraseña |
| [ ] | `POST` | `/api/v1/auth/forgot-password` | Solicitar recuperación |
| [ ] | `POST` | `/api/v1/auth/reset-password` | Restablecer contraseña |
| [ ] | `GET` | `/api/v1/auth/sessions` | Ver sesiones propias (futuro) |
| [ ] | `DELETE` | `/api/v1/auth/sessions/{id}` | Cerrar otra sesión (futuro) |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
