# Roadmap y criterios de terminado

| Etapa | Entregable |
|---|---|
| 0 | Revisar esquema y entorno, convenciones, Laravel API y conexión PostgreSQL |
| 1 | Autenticación, usuarios, roles, permisos |
| 2 | Coordinaciones, reuniones, maestros |
| 3 | Niños, tutores, vínculo y autorización de recogida |
| 4 | Sesiones con estados operativos |
| 5 | Emisión, lectura, revocación y reemplazo QR |
| 6 | Entrada/salida transaccionales y movimientos |
| 7 | Presencias, conteos, dashboard |
| 8 | Incidencias y correcciones auditadas (controles mínimos desde fases anteriores) |
| 9 | Reportes y exportaciones |
| 10 | Notificaciones, importación/fusión, mejoras avanzadas |

## Definition of Done por funcionalidad

- [ ] Regla de negocio y permiso aprobados.
- [ ] Modelo/migración revisados, sin pérdida de historial.
- [ ] Endpoint documentado con OpenAPI, payloads y errores.
- [ ] Controlador, validación, servicio y Resource implementados según necesidad.
- [ ] Pruebas positivas, negativas y acceso indebido; transacciones y concurrencia si aplica.
- [ ] Integración con React comprobada.
- [ ] Actualizado [checklist de rutas](../04-api/ENDPOINTS_CHECKLIST.md).

## Piloto con menores

No comenzar sin revisión de recogida autorizada, revocación QR, correcciones seguras, trazabilidad, respaldo/restauración y protocolo de contingencia.
