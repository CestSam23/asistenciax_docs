# Asistencias

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Una fila por niño/sesión, UNIQUE fk_id_niño + fk_id_sesion. Estados PRESENTE, RETIRADO, CANCELADO. Entrada y salida en transacción con movimiento inmutable, usuario tomado de sesión, bloqueo contra carrera, revalidación de tutores al finalizar. Idempotency-Key para reintentos. Reingreso ordinario no permitido provisionalmente.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/asistencias` | Buscar/listar |
| [ ] | `GET` | `/api/v1/asistencias/{id}` | Detalle |
| [ ] | `POST` | `/api/v1/asistencias/entradas` | Registrar entrada |
| [ ] | `POST` | `/api/v1/asistencias/salidas` | Registrar salida |
| [ ] | `GET` | `/api/v1/asistencias/{id}/movimientos` | Movimientos |
| [ ] | `POST` | `/api/v1/asistencias/{id}/cancelar` | Cancelar (restringido) |
| [ ] | `POST` | `/api/v1/asistencias/{id}/correcciones` | Corregir (restringido) |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
