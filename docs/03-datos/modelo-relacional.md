# Modelo relacional y cambios propuestos

## Doce tablas originales

| Tabla | Datos/relaciones principales |
|---|---|
| `roles` | `id`, `nombre` |
| `coordinaciones` | `id`, `nombre` |
| `reuniones` | `id`, `nombre`, `descripcion` |
| `usuarios` | `id`, `correo`, **`contrasena`**, `fk_rol`, `activo`, timestamps |
| `maestros` | `id_maestro`, nombre, apellidos, teléfono, `fk_id_usuario`, `fk_id_coordinacion` |
| `tutores` | `id_tutor`, nombre, apellidos, correo, teléfono, activo, timestamps |
| `niños` | `id_niño`, nombre, apellidos, nacimiento, `fk_id_coordinacion`, timestamps |
| `niños_tutores` | `id_niños_tutor`, `fk_niño`, `fk_tutor`, `parentesco`, `puede_recoger`, `es_contacto_principal` |
| `credenciales_qr` | `id_credencial`, FK niño/tutor excluyentes, `token_hash`, tipo, expiración, activo, `revoked_at` |
| `sesiones` | `id_sesion`, `fk_id_reunion`, fecha, horarios |
| `asistencias` | `id_asistencia`, niño, sesión, coordinación histórica, estado, horas, personal entrada/salida, tutor salida |
| `movimientos_asistencia` | `id_movimientos`, tipo, fecha_hora, usuario, tutor, asistencia |

**Atención:** documentación anterior usaba `password`, pero en trabajo posterior del proyecto el usuario confirmó **la columna real `usuarios.contrasena`**, no `password`. Se debe inspeccionar migración/DB actual antes de codificar. Laravel Auth requiere adaptar el modelo a este nombre si se mantiene. No ejecutar migraciones destructivas sobre la BD existente.

## Integridad indispensable

- `UNIQUE(fk_id_niño, fk_id_sesion)` en asistencias.
- Tipos QR `TUTOR` / `NIÑO`; exactamente uno de los FK para el titular; hash de token único; revocación efectiva.
- Salida requiere asistencia `PRESENTE`, tutor activo, vínculo activo y `puede_recoger=true`; condición verificada por servicio transaccional.
- Movimientos con historial preservado; tiempos y usuario obtenidos del backend.
- No borrar históricos en cascada accidentalmente.

## Extensiones propuestas, aún no aprobadas

1. `activo` en `niños_tutores`, `niños`, `maestros`, coordinaciones/reuniones.
2. `estado` en `sesiones`: PROGRAMADA, ABIERTA, EN_CIERRE, CERRADA, CANCELADA.
3. Auditoría administrativa separada de movimientos de asistencia.
4. Incidencias y correcciones con motivo/autorización.
5. Idempotencia de entradas/salidas.
6. Asignaciones múltiples de maestros (si la operación lo exige).
7. Notificaciones/exportaciones para etapas posteriores.

## Migraciones Laravel

Mantener script SQL como referencia, validar esquema real antes de migrar, elegir convención de identificadores y hacer migraciones versionadas. Evitar `migrate:fresh` sobre información real.
