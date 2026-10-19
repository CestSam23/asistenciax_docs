# Coordinaciones

**Prioridad:** Alta. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Orugas (3), Cachorros (4–5), Abejas (6–8), Leones (9–10), Águilas (11–12). Guardar coordinación en niño y snapshot en asistencia. Cambios de coordinación requieren revisión; no reasignación automática por cumpleaños.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/coordinaciones` | Listar |
| [ ] | `POST` | `/api/v1/coordinaciones` | Crear |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/coordinaciones/{id}` | Editar |
| [ ] | `POST` | `/api/v1/coordinaciones/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/coordinaciones/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}/ninos` | Niños del grupo |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}/maestros` | Maestros del grupo |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
