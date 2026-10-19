# Flujos operativos

## Antes del servicio

Crear/abrir sesión → autenticación del personal → selección explícita de sesión (y coordinación cuando corresponda).

## Entrada con QR tutor

Personal escanea QR de tutor → Laravel valida token, tutor, permisos → lista niños relacionados → el personal selecciona niño → backend verifica sesión/estado → crea asistencia `PRESENTE` y movimiento `ENTRADA` en una transacción.

## Entrada con QR niño

Personal escanea QR niño → backend resuelve identidad y coordinación → confirma niño y sesión → entrada bajo mismas reglas.

## Salida

Personal escanea QR de tutor (o busca manualmente bajo contingencia) → selecciona niño con asistencia `PRESENTE` → verifica físicamente identidad del adulto → Laravel **revalida** tutor activo, vínculo activo, `puede_recoger`, estado y permisos → registra `RETIRADO`, hora, usuario y tutor + movimiento `SALIDA` dentro de transacción. **El QR infantil nunca basta para la entrega.**

## Nueva familia

Registro de tutor → uno o más niños → vínculos/autorizaciones → emisión segura de QR → entrada. Propuesta: wizard de registro rápido, sin omitir verificaciones.

## Al terminar

Sesión `EN_CIERRE`: entradas ordinarias suspendidas, salidas continúan → revisar niños presentes/incidencias → cierre cuando todos estén resueltos.

## Excepciones

- QR perdido: revocar y reemplazar, comprobar identidad.
- Tutor no autorizado: rechazar, registrar incidencia y escalar.
- Error de asistencia: corrección con motivo, permiso y auditoría.
- Sin red: protocolo manual con conciliación posterior. **No prometer escrituras offline automáticas** sin estrategia de conflictos y autorización vigente.
- Concurrencia: bloqueo/atomicidad y clave de idempotencia para reintentos.

## Decisión pendiente

Reingresos en una misma sesión: propuesta inicial **no permitidos** salvo operación especial; requiere validación operativa.
