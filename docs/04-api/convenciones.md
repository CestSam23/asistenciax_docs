# Convenciones del contrato REST

**Carácter:** borrador v0.1. Endpoints exactos y JSON completos se formalizarán en OpenAPI 3.1 por fases.

## Base y transporte

- Ruta base `/api/v1`, JSON por HTTPS.
- Excepción Sanctum: `GET /sanctum/csrf-cookie` para cookie CSRF.
- SPA propia: sesión/cookies HttpOnly Secure, CSRF, CORS y mismo dominio registrable cuando aplique.
- Paginación y filtrado, p. ej. `GET /api/v1/ninos?search=ana&coordinacion_id=3&page=1&per_page=20`.
- Identificadores en rutas sin acentos; fechas en formato ISO 8601 con zona.
- No aceptar `usuario_id` enviado por cliente como autor de operaciones: tomar de `auth()->user()`.
- Idempotency-Key (UUID) en POST de entradas y salidas y operaciones no repetibles.

## Respuestas ejemplo, sujetos a contrato definitivo

```json
{"data":{"id":125,"nombre":"Ejemplo"},"message":"Registro obtenido"}
```

```json
{"message":"El niño ya tiene entrada en esta sesión","code":"ASISTENCIA_YA_REGISTRADA"}
```

## Errores HTTP

- 200 OK; 201 creado; 204 sin contenido; 400 error de petición.
- 401 sin autenticación; 403 sin permiso; 404 inexistente o no visible.
- 409 conflicto de estado/idempotencia; 422 validación/regla; 429 límite de peticiones; 500 error interno.
- Mantener códigos de negocio consistentes: `QR_EXPIRADO`, `QR_REVOCADO`, `TUTOR_NO_AUTORIZADO`, `ASISTENCIA_YA_REGISTRADA`, `ASISTENCIA_NO_PRESENTE`, `SESION_NO_ABIERTA`, etc. Todos son **propuestos**, no implementados.

## Ficha obligatoria por endpoint

Método + ruta, actor/permiso, objetivo, request, response, filtros, errores, estados, efectos secundarios, auditoría, transacción/idempotencia, pruebas y estado de implementación.

[Ir al concentrado y checklist](ENDPOINTS_CHECKLIST.md).
