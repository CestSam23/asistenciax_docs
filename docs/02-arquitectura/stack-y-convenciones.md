# Arquitectura y stack

## Arquitectura acordada

- **Dos repos Git** de implementación: `asistenciax-back` (Laravel/PHP) y `asistenciax-front` (React/TypeScript/Vite). Documentación en `asistenciax_docs`.
- Backend **monolito modular** en Laravel: API REST JSON con prefijo `/api/v1`, Eloquent, Form Requests, Resources, Policies/Gates, Services, Jobs/Notifications donde aporten valor.
- Frontend React + TypeScript + Vite, estilos Tailwind propuestos; React no accede directamente a PostgreSQL.
- **PostgreSQL** como fuente de verdad; migraciones Laravel preferibles al SQL manual definitivo.
- Autenticación propuesta: **Sanctum para SPA first-party mediante cookies, sesiones y CSRF**, evitando JWT salvo necesidad demostrada.
- Infraestructura inicial simple; Docker/colas/Redis solo según necesidades. Polling para conteos antes de WebSockets.

## Convenciones

- API en español sin acentos: `/ninos`, `/tutores`.
- SQL original en español con `ñ` (`niños`, `id_niño`), **normalización pendiente de decisión**; no renombrar silenciosamente.
- Métodos: GET consulta; POST creación/acciones; PATCH actualización; DELETE solo donde no comprometa historial.
- Respuestas API Resources con datos mínimos según roles; no revelar tokens QR originales.
- Marca tiempo auditables consistentes; propuesta `TIMESTAMPTZ` y visualización `America/Mexico_City`.
- Las rutas y contratos aún son borrador, no constatación del código.

## Estado conocido del entorno

Se informó que Laravel está inicializado en Linux, con `.env` PostgreSQL: `DB_CONNECTION=pgsql`, `DB_HOST=127.0.0.1`, `DB_PORT=5432`, `DB_DATABASE=asistenciax`, `DB_USERNAME=asistenciax_user`. No guardar ni repetir secretos; no se ha verificado el estado actual del repositorio o migraciones. Frontend indicado como inicializado.
