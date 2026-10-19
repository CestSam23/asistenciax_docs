# Configuración y operación

**Prioridad:** Alta. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Parámetros operativos bajo permisos; reglas críticas de protección infantil no editables arbitrariamente. Salud mínima pública sin detalles internos; respaldos, restauración y monitoreo como procesos operacionales no API expuesta.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/configuracion` | Consultar parámetros |
| [ ] | `PATCH` | `/api/v1/configuracion` | Editar parámetros |
| [ ] | `GET` | `/api/v1/sistema/estado` | Estado operacional restringido |
| [ ] | `GET` | `/api/v1/sistema/version` | Versión servicio |
| [ ] | `GET` | `/api/v1/health` | Health mínimo |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
