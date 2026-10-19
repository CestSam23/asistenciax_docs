# Decisiones pendientes (no asumir resueltas)

| ID | Pregunta | Propuesta actual |
|---|---|---|
| DEC-01 | ¿Reingreso a misma sesión? | No ordinario, salvo excepción auditada |
| DEC-02 | ¿Sesiones simultáneas? | Sí, selección explícita y control de duplicidades |
| DEC-03 | ¿Maestro en múltiples coordinaciones/reuniones? | Prever asignaciones, validar con operación |
| DEC-04 | ¿Quién modifica autorizaciones? | Admin y coordinador expresamente facultado |
| DEC-05 | ¿Operación sin QR? | Búsqueda manual, verificación física y auditoría |
| DEC-06 | ¿Cerrar sesión con niños presentes? | No ordinariamente |
| DEC-07 | ¿Emisión/entrega de QR? | Entrega verificada; token revelado solo emisión |
| DEC-08 | ¿Niño nuevo sin tutor registrado? | Flujo alta+autorización, no entrada/salida insegura |
| DEC-09 | ¿Incidencias de custodia? | Escalamiento físico y registro controlado |
| DEC-10 | ¿Conservar `ñ` en SQL? | Evaluar cambio controlado previo a migraciones |
| DEC-11 | ¿Modelo `usuarios` en Laravel? | Adaptar Auth al esquema real `contrasena`, no `password` |
| DEC-12 | ¿Recuperación contraseñas desde MVP? | Definir correo vs procedimiento administrativo |
| DEC-13 | ¿Datos médicos o alergias? | Solo si son imprescindibles, permisos/retención estrictos |
| DEC-14 | ¿Retención y borrado de datos? | Definir política legal y organizacional |
| DEC-15 | ¿Cómo se contabilizan niños entre sesiones abiertas? | Separar asistencias vs niños únicos |

## Verificación del estado real

Antes de modificar el backend consultar `php artisan --version`, `php artisan route:list`, migraciones existentes, columnas reales y pruebas. No confiar en documentación conversacional para inferir que algo ya fue desplegado.
