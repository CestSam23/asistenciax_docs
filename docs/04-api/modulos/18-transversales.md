# Operaciones transversales

**Prioridad:** Propuesta. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Registro rápido familiar transaccional; búsqueda global segura; posibles duplicados, fusiones auditadas, importaciones con vista previa. No implementar fusiones automáticas inicialmente.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `POST` | `/api/v1/registros/familias` | Registro rápido familiar |
| [ ] | `GET` | `/api/v1/busquedas/personas` | Búsqueda global |
| [ ] | `GET` | `/api/v1/ninos/posibles-duplicados` | Posibles duplicados niños |
| [ ] | `GET` | `/api/v1/tutores/posibles-duplicados` | Posibles duplicados tutores |
| [ ] | `POST` | `/api/v1/ninos/fusiones` | Fusión administrativa niños |
| [ ] | `POST` | `/api/v1/tutores/fusiones` | Fusión administrativa tutores |
| [ ] | `POST` | `/api/v1/importaciones` | Subir importación |
| [ ] | `GET` | `/api/v1/importaciones/{id}` | Estado importación |
| [ ] | `POST` | `/api/v1/importaciones/{id}/confirmar` | Confirmar importación |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
