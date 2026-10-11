# Guía de trabajo del equipo

## Ramas

| Rama | Uso |
|---|---|
| `main` | Versión estable. Solo recibe cambios desde `develop` mediante Pull Request. |
| `develop` | Integración del equipo. |
| `feature/*` | Una rama por funcionalidad (por ejemplo `feature/auth`, `feature/derivaciones`). |
| `hotfix/*` | Correcciones urgentes sobre `main`. |

## Flujo de trabajo

1. Crea tu rama desde `develop`: `feature/nombre-de-la-tarea`.
2. Haz tus cambios y guarda con commits pequeños.
3. Abre un **Pull Request** hacia `develop`.
4. Otra integrante lo revisa y lo aprueba antes de unirlo (revisión cruzada).
5. Cuando `develop` esté estable, se abre un Pull Request hacia `main`.

## Mensajes de commit (Conventional Commits)

Formato: `tipo: descripción corta en español`

| Tipo | Cuándo usarlo |
|---|---|
| `feat:` | Nueva funcionalidad |
| `fix:` | Corrección de un error |
| `docs:` | Documentación |
| `style:` | Formato, sin cambiar la lógica |
| `refactor:` | Reorganizar código sin cambiar el resultado |
| `test:` | Pruebas |
| `chore:` | Tareas de mantenimiento |

Ejemplos: `feat: agrega formulario de nueva solicitud`, `docs: actualiza README`.

## Acuerdos del equipo

- Mínimo 3 commits por semana por integrante, en su rama `feature/*`.
- Reunión semanal los lunes a las 19:00 h por Google Meet.
- Las tareas se organizan en GitHub Issues.

## Seguridad

- No subir `.env`, contraseñas, llaves ni datos reales de personas.
- Usar solo datos de prueba.
