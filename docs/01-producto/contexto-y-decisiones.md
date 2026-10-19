# Contexto, alcance y decisiones

## Producto

AsistenciaX administra entradas y salidas de niños en AX (Adoradores Extremos de Jesús), ministerio infantil de Amistad de Puebla. Escala de diseño: aproximadamente **500–600 niños por jornada** y **100 maestros/colaboradores**.

## Actores

- Solo el personal autenticado opera el sistema: **Administrador, Coordinador, Maestro y Apoyo**.
- **Los tutores NO tienen cuentas**, NO escanean para operar, NO registran entradas/salidas; presentan QR al personal y recogen físicamente al niño.
- Los niños son sujetos del registro, no usuarios del sistema.

## Coordinaciones

| Orugas | Cachorros | Abejas | Leones | Águilas |
|---|---|---|---|---|
| 3 años | 4–5 | 6–8 | 9–10 | 11–12 |

## Acuerdos estables

- Dos QR: **TUTOR** y **NIÑO**; token aleatorio opaco, revocable. QR de niño **no autoriza** salida.
- Identidad del tutor verificada físicamente en toda entrega.
- `reuniones` son tipos (Primera, Segunda, Inter); `sesiones` son instancias fechadas.
- Una asistencia por niño y sesión; asistencias distintas el mismo día sí son posibles.
- Estados de asistencia: `PRESENTE`, `RETIRADO`, `CANCELADO`.
- Movimientos: `ENTRADA`, `SALIDA`, `CORRECCION`, `CANCELACION`.
- Historial preservado, operaciones críticas atómicas, conteo de presentes, contingencia ante falla de red.
- No existe una tabla `solicitudes_salida`: el personal autorizado registra la salida directamente.

## Alcance

MVP con personal, registros, vínculos, sesiones, QR, entradas, salidas, monitoreo, revocación, corrección auditada e incidencias básicas. Reportes complejos, importaciones/fusiones y notificaciones extensas son evolución futura.
