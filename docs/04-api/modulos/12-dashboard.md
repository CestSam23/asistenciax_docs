# Control operativo

**Prioridad:** Crítica. **Estado:** contrato propuesto; sin verificación de implementación.

## Alcance y reglas

Conteos por sesión y coordinación, niños PRESENTE, actividad reciente, alertas y polling desde React. Reuniones simultáneas: evitar sumar personas dos veces al calcular niños distintos. Acceso a datos personales mínimo.

## Endpoints del módulo

| Estado | Método | Ruta | Función |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/dashboard/resumen` | Resumen global |
| [ ] | `GET` | `/api/v1/sesiones/{id}/dashboard` | Dashboard sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/presentes` | Presentes (compartido con otro módulo) |
| [ ] | `GET` | `/api/v1/sesiones/{id}/conteos` | Conteos por coordinación |
| [ ] | `GET` | `/api/v1/sesiones/{id}/movimientos-recientes` | Movimientos recientes |
| [ ] | `GET` | `/api/v1/sesiones/{id}/alertas` | Alertas |

## Antes de implementar

- [ ] Cerrar validaciones y permisos exactos.
- [ ] Definir request y response JSON (incluidos errores).
- [ ] Crear migraciones/modelos cuando aplique.
- [ ] Implementar Policies, Form Requests, Services y API Resources según responsabilidad.
- [ ] Añadir pruebas exitosas, de error, autorización y concurrencia cuando aplique.
- [ ] Actualizar el concentrado de endpoints y OpenAPI.

**Nota:** las rutas son propuestas, no una declaración del código existente.
