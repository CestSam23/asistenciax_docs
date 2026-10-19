# Relaciones niño-tutor

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Muchos a muchos con parentesco, es_contacto_principal, puede_recoger y activo propuesto. Autorizar salida solo con tutor activo y vínculo activo con puede_recoger=true. Cambios sensibles auditados, no improvisar autorización durante recogida.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores` | Listar vínculos (compartido con otro módulo) |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores` | Vincular tutor |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores/{tutorId}` | Detalle vínculo |
| [ ] | `PATCH` | `/api/v1/ninos/{id}/tutores/{tutorId}` | Editar permisos/vínculo |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores/{tutorId}/activar` | Reactivar relación |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores/{tutorId}/desactivar` | Desactivar relación |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores-autorizados` | Lista autorizados |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
