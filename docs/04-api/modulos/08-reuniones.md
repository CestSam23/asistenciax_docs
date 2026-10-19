# Reuniones

**Prioridad:** Alta. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Reunión es tipo de reunión, distinto de sesión fechada. Semillas: Primera Reunión, Segunda Reunión, Inter. Eventos especiales pueden ser reuniones adicionales.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/reuniones` | Listar |
| [ ] | `POST` | `/api/v1/reuniones` | Crear |
| [ ] | `GET` | `/api/v1/reuniones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/reuniones/{id}` | Editar |
| [ ] | `POST` | `/api/v1/reuniones/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/reuniones/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/reuniones/{id}/sesiones` | Sesiones relacionadas |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
