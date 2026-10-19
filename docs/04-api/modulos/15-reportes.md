# Reportes

**Prioridad:** Media. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Diferenciar número de asistencias y niños únicos. Filtros por periodo, reunión y coordinación. Exportación protegida, con expiración y registro de responsable. Cálculos agregados, privilegios restringidos.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/reportes/asistencia-general` | Resumen general |
| [ ] | `GET` | `/api/v1/reportes/asistencia-por-coordinacion` | Por coordinación |
| [ ] | `GET` | `/api/v1/reportes/asistencia-por-reunion` | Por reunión |
| [ ] | `GET` | `/api/v1/reportes/asistencia-por-periodo` | Por fechas |
| [ ] | `GET` | `/api/v1/reportes/frecuencia-ninos` | Frecuencia |
| [ ] | `GET` | `/api/v1/reportes/ninos-sin-asistencia` | Inactivos recientes |
| [ ] | `GET` | `/api/v1/reportes/primeras-asistencias` | Primera asistencia |
| [ ] | `GET` | `/api/v1/reportes/operacion` | Indicadores operación |
| [ ] | `POST` | `/api/v1/reportes/exportaciones` | Solicitar exportación |
| [ ] | `GET` | `/api/v1/reportes/exportaciones/{id}` | Estado exportación |
| [ ] | `GET` | `/api/v1/reportes/exportaciones/{id}/descargar` | Descargar exportación |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
