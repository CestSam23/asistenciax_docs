# Niños

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Registro, búsqueda paginada, actualización controlada, baja lógica y consulta de tutores y asistencias. Duplicados: sugerir coincidencias y confirmar manualmente, no fusionar automáticamente. Campos sensibles solo si existe necesidad operativa y protección específica.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/ninos` | Buscar/listar |
| [ ] | `POST` | `/api/v1/ninos` | Registrar |
| [ ] | `GET` | `/api/v1/ninos/{id}` | Expediente |
| [ ] | `PATCH` | `/api/v1/ninos/{id}` | Editar |
| [ ] | `POST` | `/api/v1/ninos/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/ninos/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores` | Tutores |
| [ ] | `GET` | `/api/v1/ninos/{id}/asistencias` | Historial |
| [ ] | `GET` | `/api/v1/ninos/{id}/estado-actual` | Estado en sesión |
| [ ] | `GET` | `/api/v1/ninos/{id}/credenciales` | Credenciales, sin secretos |
| [ ] | `PATCH` | `/api/v1/ninos/{id}/coordinacion` | Cambiar coordinación |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
