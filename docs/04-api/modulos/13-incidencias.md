# Incidencias y correcciones

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Incidencias: QR_EXTRAVIADO, QR_INVALIDO, TUTOR_NO_AUTORIZADO, ERROR_ENTRADA, ERROR_SALIDA, NINO_NO_LOCALIZADO, FALLA_CONECTIVIDAD, OTRA. Corrección con motivo y responsable, autorización especial cuando corresponda; no PATCH libre de estados. Búsqueda manual verifica identidad y permisos.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/incidencias` | Listar |
| [ ] | `POST` | `/api/v1/incidencias` | Registrar |
| [ ] | `GET` | `/api/v1/incidencias/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/incidencias/{id}` | Actualizar datos permitidos |
| [ ] | `POST` | `/api/v1/incidencias/{id}/resolver` | Resolver |
| [ ] | `POST` | `/api/v1/incidencias/{id}/cerrar` | Cerrar |
| [ ] | `GET` | `/api/v1/asistencias/{id}/correcciones` | Historial de correcciones |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
