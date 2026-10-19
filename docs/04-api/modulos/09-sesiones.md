# Sesiones

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Sesión = instancia de reunión con fecha y horario. Estados propuestos PROGRAMADA, ABIERTA, EN_CIERRE, CERRADA, CANCELADA. Seleccionar sesión explícitamente en cliente; cerrar ordinariamente solo sin niños presentes. Sesiones simultáneas y reglas de transferencia pendientes.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/sesiones` | Listar |
| [ ] | `POST` | `/api/v1/sesiones` | Crear |
| [ ] | `GET` | `/api/v1/sesiones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/sesiones/{id}` | Editar |
| [ ] | `GET` | `/api/v1/sesiones/actuales` | Operativas actuales |
| [ ] | `POST` | `/api/v1/sesiones/{id}/abrir` | Abrir |
| [ ] | `POST` | `/api/v1/sesiones/{id}/cerrar` | Cerrar |
| [ ] | `POST` | `/api/v1/sesiones/{id}/cancelar` | Cancelar |
| [ ] | `POST` | `/api/v1/sesiones/{id}/reabrir` | Reabrir excepcional |
| [ ] | `GET` | `/api/v1/sesiones/{id}/resumen` | Resumen |
| [ ] | `GET` | `/api/v1/sesiones/{id}/asistencias` | Asistencias sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/presentes` | Presentes sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/incidencias` | Incidencias sesión |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
