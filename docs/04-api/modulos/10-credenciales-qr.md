# Credenciales QR

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Dos tipos TUTOR y NINO; token aleatorio opaco >=32 bytes, SHA-256 de token guardado, titular único por credencial, revocación/expiración. Token original solo en emisión; prevenir logs y URL públicos. Escáner de React entrega token a Laravel autenticado. QR de niño NO autoriza salida.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `POST` | `/api/v1/qr/resolver` | Validar token y resolver tipo |
| [ ] | `GET` | `/api/v1/credenciales-qr` | Inventario sin secretos |
| [ ] | `POST` | `/api/v1/tutores/{id}/credenciales-qr` | Generar QR tutor |
| [ ] | `POST` | `/api/v1/ninos/{id}/credenciales-qr` | Generar QR niño |
| [ ] | `GET` | `/api/v1/tutores/{id}/credenciales-qr` | Credenciales tutor |
| [ ] | `GET` | `/api/v1/ninos/{id}/credenciales-qr` | Credenciales niño |
| [ ] | `POST` | `/api/v1/credenciales-qr/{id}/revocar` | Revocar |
| [ ] | `POST` | `/api/v1/credenciales-qr/{id}/reemplazar` | Reemplazar |
| [ ] | `POST` | `/api/v1/credenciales-qr/{id}/entregar` | Registrar entrega (propuesta) |
| [ ] | `GET` | `/api/v1/credenciales-qr/{id}/historial` | Historial credencial |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
