# Notificaciones

**Prioridad:** Media. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Avisos internos por incidencias, correcciones pendientes, cierre de sesiones, credenciales. Correos solo por canales verificados, colas Laravel para tareas asíncronas. No enviar QR de menores indiscriminadamente.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/notificaciones` | Listar |
| [ ] | `GET` | `/api/v1/notificaciones/no-leidas` | No leídas |
| [ ] | `POST` | `/api/v1/notificaciones/{id}/marcar-leida` | Marcar leída |
| [ ] | `POST` | `/api/v1/notificaciones/marcar-todas-leidas` | Marcar todas |
| [ ] | `GET` | `/api/v1/notificaciones/preferencias` | Preferencias |
| [ ] | `PATCH` | `/api/v1/notificaciones/preferencias` | Editar preferencias |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
