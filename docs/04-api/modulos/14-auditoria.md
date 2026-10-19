# Auditoría

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Movimientos de asistencia != auditoría administrativa. Auditoría de cambios de rol, autorizaciones de recogida, QR, correcciones y bajas. Sin endpoints públicos para borrar/modificar eventos. Excluir contraseñas y secretos.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/auditoria` | Consultar auditoría |
| [ ] | `GET` | `/api/v1/auditoria/{id}` | Detalle evento |
| [ ] | `GET` | `/api/v1/usuarios/{id}/actividad` | Actividad usuario |
| [ ] | `GET` | `/api/v1/credenciales-qr/{id}/historial` | Historial QR (compartido con otro módulo) |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
