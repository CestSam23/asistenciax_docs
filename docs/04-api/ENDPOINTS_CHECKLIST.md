# Concentrado de endpoints y checklist de implementación

**Versión:** 0.1 · **Actualización:** 2026-10-18 · **Estado:** propuesta funcional.

> **Criterio:** `[ ]` = **pendiente de verificar/implementar**; no significa necesariamente que la funcionalidad no exista en otro repositorio. Ningún endpoint se marca completado sin contrastar Laravel, pruebas y, cuando corresponda, React.

## Criterios para marcar `[x]`

1. Ruta registrada en Laravel y accesible en entorno de prueba.
2. Autenticación/autorización implementadas y verificadas.
3. Request, response, errores y filtros acordados.
4. Pruebas automatizadas pasando (casos positivos, negativos, permisos y concurrencia si aplica).
5. Contrato documentado y revisado con frontend.

**Prefijo:** `/api/v1` excepto `/sanctum/csrf-cookie`. Algunas rutas figuran en varios módulos; este índice deduplica por método+ruta.

## Autenticación — Crítica

[Especificación del módulo](modulos/01-autenticacion.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [✔️] | `GET` | `/sanctum/csrf-cookie` | Obtener cookie CSRF |
| [✔️] | `POST` | `/api/v1/auth/login` | Iniciar sesión |
| [✔️] | `POST` | `/api/v1/auth/logout` | Cerrar sesión |
| [✔️] | `GET` | `/api/v1/auth/me` | Usuario y permisos |
| [✔️] | `POST` | `/api/v1/auth/change-password` | Cambiar contraseña |
| [✔️] | `POST` | `/api/v1/auth/forgot-password` | Solicitar recuperación |
| [✔️] | `POST` | `/api/v1/auth/reset-password` | Restablecer contraseña |
| [ ] | `GET` | `/api/v1/auth/sessions` | Ver sesiones propias (futuro) |
| [ ] | `DELETE` | `/api/v1/auth/sessions/{id}` | Cerrar otra sesión (futuro) |

## Usuarios, roles y permisos — Crítica

[Especificación del módulo](modulos/02-usuarios-permisos.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/usuarios` | Listar usuarios |
| [ ] | `POST` | `/api/v1/usuarios` | Crear usuario |
| [ ] | `GET` | `/api/v1/usuarios/{id}` | Consultar usuario |
| [ ] | `PATCH` | `/api/v1/usuarios/{id}` | Actualizar usuario |
| [ ] | `POST` | `/api/v1/usuarios/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/usuarios/{id}/desactivar` | Desactivar |
| [ ] | `POST` | `/api/v1/usuarios/{id}/reset-password` | Reset administrativo |
| [ ] | `GET` | `/api/v1/roles` | Roles |
| [ ] | `GET` | `/api/v1/roles/{id}/permisos` | Permisos del rol |
| [ ] | `PUT` | `/api/v1/roles/{id}/permisos` | Configurar permisos (propuesta) |
| [ ] | `GET` | `/api/v1/permisos` | Catálogo permisos |

## Coordinaciones — Alta

[Especificación del módulo](modulos/03-coordinaciones.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/coordinaciones` | Listar |
| [ ] | `POST` | `/api/v1/coordinaciones` | Crear |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/coordinaciones/{id}` | Editar |
| [ ] | `POST` | `/api/v1/coordinaciones/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/coordinaciones/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}/ninos` | Niños del grupo |
| [ ] | `GET` | `/api/v1/coordinaciones/{id}/maestros` | Maestros del grupo |

## Maestros — Alta

[Especificación del módulo](modulos/04-maestros.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/maestros` | Listar |
| [ ] | `POST` | `/api/v1/maestros` | Registrar |
| [ ] | `GET` | `/api/v1/maestros/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/maestros/{id}` | Editar |
| [ ] | `POST` | `/api/v1/maestros/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/maestros/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/maestros/{id}/asignaciones` | Asignaciones |
| [ ] | `PUT` | `/api/v1/maestros/{id}/asignaciones` | Cambiar asignaciones (propuesta) |

## Niños — Crítica

[Especificación del módulo](modulos/05-ninos.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/ninos` | Buscar/listar |
| [ ] | `POST` | `/api/v1/ninos` | Registrar |
| [ ] | `GET` | `/api/v1/ninos/{id}` | Expediente |
| [ ] | `PATCH` | `/api/v1/ninos/{id}` | Editar |
| [ ] | `POST` | `/api/v1/ninos/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/ninos/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores` | Tutores |
| [ ] | `GET` | `/api/v1/ninos/{id}/asistencias` | Historial |
| [ ] | `GET` | `/api/v1/ninos/{id}/estado-actual` | Estado en sesión |
| [ ] | `GET` | `/api/v1/ninos/{id}/credenciales` | Credenciales, sin secretos |
| [ ] | `PATCH` | `/api/v1/ninos/{id}/coordinacion` | Cambiar coordinación |

## Tutores — Crítica

[Especificación del módulo](modulos/06-tutores.md)

| Hecho | Método | Ruta | Funcionalidad |
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

## Relaciones niño-tutor — Crítica

[Especificación del módulo](modulos/07-relaciones.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores` | Listar vínculos |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores` | Vincular tutor |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores/{tutorId}` | Detalle vínculo |
| [ ] | `PATCH` | `/api/v1/ninos/{id}/tutores/{tutorId}` | Editar permisos/vínculo |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores/{tutorId}/activar` | Reactivar relación |
| [ ] | `POST` | `/api/v1/ninos/{id}/tutores/{tutorId}/desactivar` | Desactivar relación |
| [ ] | `GET` | `/api/v1/ninos/{id}/tutores-autorizados` | Lista autorizados |

## Reuniones — Alta

[Especificación del módulo](modulos/08-reuniones.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/reuniones` | Listar |
| [ ] | `POST` | `/api/v1/reuniones` | Crear |
| [ ] | `GET` | `/api/v1/reuniones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/reuniones/{id}` | Editar |
| [ ] | `POST` | `/api/v1/reuniones/{id}/activar` | Activar |
| [ ] | `POST` | `/api/v1/reuniones/{id}/desactivar` | Desactivar |
| [ ] | `GET` | `/api/v1/reuniones/{id}/sesiones` | Sesiones relacionadas |

## Sesiones — Crítica

[Especificación del módulo](modulos/09-sesiones.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/sesiones` | Listar |
| [ ] | `POST` | `/api/v1/sesiones` | Crear |
| [ ] | `GET` | `/api/v1/sesiones/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/sesiones/{id}` | Editar |
| [ ] | `GET` | `/api/v1/sesiones/actuales` | Operativas actuales |
| [ ] | `POST` | `/api/v1/sesiones/{id}/abrir` | Abrir |
| [ ] | `POST` | `/api/v1/sesiones/{id}/cerrar` | Cerrar |
| [ ] | `POST` | `/api/v1/sesiones/{id}/cancelar` | Cancelar |
| [ ] | `POST` | `/api/v1/sesiones/{id}/reabrir` | Reabrir excepcional |
| [ ] | `GET` | `/api/v1/sesiones/{id}/resumen` | Resumen |
| [ ] | `GET` | `/api/v1/sesiones/{id}/asistencias` | Asistencias sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/presentes` | Presentes sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/incidencias` | Incidencias sesión |

## Credenciales QR — Crítica

[Especificación del módulo](modulos/10-credenciales-qr.md)

| Hecho | Método | Ruta | Funcionalidad |
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

## Asistencias — Crítica

[Especificación del módulo](modulos/11-asistencias.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/asistencias` | Buscar/listar |
| [ ] | `GET` | `/api/v1/asistencias/{id}` | Detalle |
| [ ] | `POST` | `/api/v1/asistencias/entradas` | Registrar entrada |
| [ ] | `POST` | `/api/v1/asistencias/salidas` | Registrar salida |
| [ ] | `GET` | `/api/v1/asistencias/{id}/movimientos` | Movimientos |
| [ ] | `POST` | `/api/v1/asistencias/{id}/cancelar` | Cancelar (restringido) |
| [ ] | `POST` | `/api/v1/asistencias/{id}/correcciones` | Corregir (restringido) |

## Control operativo — Crítica

[Especificación del módulo](modulos/12-dashboard.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/dashboard/resumen` | Resumen global |
| [ ] | `GET` | `/api/v1/sesiones/{id}/dashboard` | Dashboard sesión |
| [ ] | `GET` | `/api/v1/sesiones/{id}/presentes` | Presentes |
| [ ] | `GET` | `/api/v1/sesiones/{id}/conteos` | Conteos por coordinación |
| [ ] | `GET` | `/api/v1/sesiones/{id}/movimientos-recientes` | Movimientos recientes |
| [ ] | `GET` | `/api/v1/sesiones/{id}/alertas` | Alertas |

## Incidencias y correcciones — Crítica

[Especificación del módulo](modulos/13-incidencias.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/incidencias` | Listar |
| [ ] | `POST` | `/api/v1/incidencias` | Registrar |
| [ ] | `GET` | `/api/v1/incidencias/{id}` | Detalle |
| [ ] | `PATCH` | `/api/v1/incidencias/{id}` | Actualizar datos permitidos |
| [ ] | `POST` | `/api/v1/incidencias/{id}/resolver` | Resolver |
| [ ] | `POST` | `/api/v1/incidencias/{id}/cerrar` | Cerrar |
| [ ] | `GET` | `/api/v1/asistencias/{id}/correcciones` | Historial de correcciones |

## Auditoría — Crítica

[Especificación del módulo](modulos/14-auditoria.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/auditoria` | Consultar auditoría |
| [ ] | `GET` | `/api/v1/auditoria/{id}` | Detalle evento |
| [ ] | `GET` | `/api/v1/usuarios/{id}/actividad` | Actividad usuario |
| [ ] | `GET` | `/api/v1/credenciales-qr/{id}/historial` | Historial QR |

## Reportes — Media

[Especificación del módulo](modulos/15-reportes.md)

| Hecho | Método | Ruta | Funcionalidad |
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

## Notificaciones — Media

[Especificación del módulo](modulos/16-notificaciones.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/notificaciones` | Listar |
| [ ] | `GET` | `/api/v1/notificaciones/no-leidas` | No leídas |
| [ ] | `POST` | `/api/v1/notificaciones/{id}/marcar-leida` | Marcar leída |
| [ ] | `POST` | `/api/v1/notificaciones/marcar-todas-leidas` | Marcar todas |
| [ ] | `GET` | `/api/v1/notificaciones/preferencias` | Preferencias |
| [ ] | `PATCH` | `/api/v1/notificaciones/preferencias` | Editar preferencias |

## Configuración y operación — Alta

[Especificación del módulo](modulos/17-configuracion.md)

| Hecho | Método | Ruta | Funcionalidad |
|---|---|---|---|
| [ ] | `GET` | `/api/v1/configuracion` | Consultar parámetros |
| [ ] | `PATCH` | `/api/v1/configuracion` | Editar parámetros |
| [ ] | `GET` | `/api/v1/sistema/estado` | Estado operacional restringido |
| [ ] | `GET` | `/api/v1/sistema/version` | Versión servicio |
| [ ] | `GET` | `/api/v1/health` | Health mínimo |

## Operaciones transversales — Propuesta

[Especificación del módulo](modulos/18-transversales.md)

| Hecho | Método | Ruta | Funcionalidad |
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

## Progreso consolidado

| Etapa | Estado | Evidencia |
|---|---|---|
| Definición de reglas | En elaboración | Docs por módulo |
| Implementación Laravel | Sin verificar | Revisar `php artisan route:list --path=api` |
| Testing | Sin verificar | Revisar suite de tests |
| Integración React | Sin verificar | Revisar cliente |

**Mantenimiento:** al cerrar PR del backend, registrar ruta, prueba y actualización de documentación. No marcar por haber creado solamente el controlador.
