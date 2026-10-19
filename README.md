# AsistenciaX — Documentación

Repositorio de especificaciones funcionales y técnicas para **AsistenciaX**, plataforma de control de asistencia del ministerio infantil **AX / Amistad Niños** de la iglesia Amistad de Puebla.

> **Versión 0.1.** Las rutas son un **contrato preliminar**, no evidencia de implementación.

## Comenzar aquí

1. [Contexto y decisiones](docs/01-producto/contexto-y-decisiones.md)
2. [Flujos operativos](docs/01-producto/flujos-operativos.md)
3. [Arquitectura y convenciones](docs/02-arquitectura/stack-y-convenciones.md)
4. [Modelo de datos](docs/03-datos/modelo-relacional.md)
5. [Contrato API y errores](docs/04-api/convenciones.md)
6. **[Concentrado de rutas y checklist](docs/04-api/ENDPOINTS_CHECKLIST.md)**
7. [Seguridad y permisos](docs/05-seguridad/matriz-permisos.md)
8. [Plan de implementación](docs/06-ejecucion/roadmap.md)
9. [Decisiones pendientes](docs/06-ejecucion/decisiones-pendientes.md)

### Organización

```text
docs/
├── 01-producto/        # Alcance y procesos
├── 02-arquitectura/    # Laravel, React y convenciones
├── 03-datos/           # Tablas y restricciones
├── 04-api/             # Rutas y especificaciones por módulo
│   ├── ENDPOINTS_CHECKLIST.md
│   └── modulos/        # 18 documentos
├── 05-seguridad/       # Privacidad, QR y RBAC
└── 06-ejecucion/       # Roadmap, pruebas y pendientes
```

**Repositorios relacionados:** `asistenciax-back` (Laravel) y `asistenciax-front` (React). No almacenar datos reales de menores ni secretos en este repositorio.
