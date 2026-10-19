# Maestros

**Prioridad:** Alta. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Maestro como expediente operativo ligado opcionalmente a usuario de acceso. Posible necesidad de múltiples asignaciones por sesión/reunión y coordinación: por confirmar; no equiparar maestro con cuenta login.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/maestros` | Listar |
| [ ] | `POST` | `/api/v1/maestros` | Registrar |
| [ ] | `GET` | `/api/v1/maestros/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/maestros/{id}` | Editar |
| [ ] | `POST` | `/api/v1/maestros/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/maestros/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/maestros/{id}/asignaciones` | Asignaciones |
| [ ] | `PUT` | `/api/v1/maestros/{id}/asignaciones` | Cambiar asignaciones (propuesta) |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
