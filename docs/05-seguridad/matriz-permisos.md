# Seguridad, roles y permisos preliminares

## Regla absoluta

Solo staff autenticado opera. Tutores no tienen cuenta. El QR identifica pero **no autoriza recogida por sí solo**. Debe verificarse físicamente la identidad del adulto y validarse vínculo + permiso de recogida al confirmar salida.

## Matriz inicial (revisar con AX)

| Acción | Admin | Coordinador | Maestro | Apoyo |
|---|---|---|---|---|
| Login | Sí | Sí | Sí | Sí |
| Ver niños bajo su alcance | Sí | Sí | Sí | Limitado |
| Alta niños/tutores | Sí | Sí | Por definir | Por definir |
| Editar autorización recogida | Sí | Restringido | No | No |
| Generar QR | Sí | Sí | Por definir | No |
| Revocar QR | Sí | Restringido | No | No |
| Registrar entrada | Sí | Sí | Sí | Por definir |
| Registrar salida | Sí | Sí | Sí | Por definir |
| Corregir/cancelar asistencia | Sí | Restringido | No | No |
| Administrar sesiones | Sí | Sí | No | No |
| Ver conteos/presentes | Sí | Sí | Sí | Limitado |
| Reportes/auditoría | Sí | Limitado | No | No |
| Usuarios y roles | Sí | No | No | No |

## Controles

- Policies/Gates y middleware Laravel; control por coordinación además del rol.
- Autorizar cada operación en backend aunque React oculte un botón.
- Rate limiting en login, recuperación y resolución QR; evitar enumeración.
- Revocación QR y cambios de permisos deben surtir efecto inmediatamente en backend.
- Logs y auditoría sin secretos, contraseñas, tokens crudos ni PII excesiva.
- Correcciones/cambios de autorización con motivo y responsables; historial a prueba de alteración ordinaria.
- Restricción de exportación y política de retención; cumplir obligaciones de privacidad aplicables a menores en México.
