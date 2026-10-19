# Plan inicial de pruebas

## Auth

- [ ] Usuario activo autenticado; credenciales inválidas; cuenta desactivada; logout; acceso sin sesión; alcance por rol y coordinación.

## Registros y vínculos

- [ ] Tutor con varios niños; niño con varios tutores; `puede_recoger=false`; relación/tutor inactivos; cambios auditados; duplicados sugeridos sin fusión automática.

## QR

- [ ] Token válido, inexistente, revocado, vencido, titular inactivo; reemplazo invalida anterior; secreto no en logs/GET; rate limit; no salida solo con QR infantil.

## Sesiones y asistencias

- [ ] Entrada con sesión abierta, rechazos en estados no permitidos; entrada duplicada; salida sin entrada; salida duplicada; salida tutor no autorizado; cambio de permiso entre escaneo y salida; niños aún presentes en cierre.
- [ ] Dos peticiones concurrentes mismo niño/sesión; retry con Idempotency-Key; transacción falla completa sin generar movimiento huérfano.
- [ ] Conteos correctos por coordinación/sesión, diferenciando asistentes únicos y asistencias.

## Incidencias y reportes

- [ ] Corrección autorizada con valores previos/motivo; rechazo a cambios directos de estado; exportaciones limitadas y auditadas.
