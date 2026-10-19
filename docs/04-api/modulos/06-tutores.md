# Tutores

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Los tutores NO tienen acceso a la aplicación. Datos básicos: nombre, apellidos, correo opcional (pendiente), teléfono, activo. Un tutor puede tener varios niños. No eliminar historial por baja. QR no equivale a autorización.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/tutores` | Buscar/listar |
| [ ] | `POST` | `/api/v1/tutores` | Registrar |
| [ ] | `GET` | `/api/v1/tutores/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/tutores/{id}` | Editar |
| [ ] | `POST` | `/api/v1/tutores/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/tutores/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/tutores/{id}/ninos` | Niños vinculados |
| [ ] | `GET` | `/api/v1/tutores/{id}/credenciales` | Estado credenciales |
| [ ] | `GET` | `/api/v1/tutores/{id}/retiros` | Retiros históricos |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
