# MENTE Arequipa

Plataforma web de orientación y trazabilidad de derivaciones para jóvenes de 18 a 29 años que buscan atención en salud mental en Arequipa, Perú.

> **Importante:** esta plataforma **no es un servicio de emergencia**. Los casos de crisis se derivan a la **Línea 113, opción 5**.

Proyecto académico del curso **Programación Web** (NRC 40537), Universidad Continental, octubre de 2026.

## ¿Qué hace?

- El joven registra una solicitud de orientación con consentimiento informado digital (Ley N.° 29733).
- Un orientador revisa el caso y lo deriva a un centro de salud mental, comunitario o ONG.
- Cada cambio de estado queda registrado (REGISTRADA → EN_REVISIÓN → DERIVADA → ACEPTADA → ATENDIDA).
- El joven (o un familiar) consulta el estado con un **código anónimo**, sin iniciar sesión.

## Tecnologías

| Capa | Tecnología |
|---|---|
| Frontend | Vue 3 + Vite + Tailwind CSS |
| Backend | Laravel 12 (API REST) + Sanctum |
| Base de datos | PostgreSQL 16 |
| Despliegue | Vercel (frontend), Railway (backend), Aiven o Neon (base de datos), Cloudflare R2 (archivos) |
| CI/CD | GitHub Actions |

## Estructura del repositorio

```
mente-arequipa/
├── backend/      API REST en Laravel (se agrega desde la semana 12)
├── frontend/     SPA en Vue 3 (se agrega desde la semana 12)
├── docs/         Documentación y capturas del prototipo
│   └── capturas/
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## Instalación (disponible desde la semana 12)

Requisitos: PHP 8.2 o superior, Composer, Node.js, PostgreSQL 16.

```bash
# Backend
cd backend
composer install
cp .env.example .env        # completar las variables de entorno
php artisan key:generate
php artisan migrate --seed  # solo datos de prueba
php artisan serve

# Frontend (en otra terminal)
cd frontend
npm install
npm run dev
```

Nunca subas el archivo `.env` ni datos reales de personas. Este prototipo usa **solo datos de prueba**.

## Documentación

- Capturas del prototipo (Google Stitch): carpeta [`docs/capturas`](docs/capturas).
- Documento de Fases 1 y 2: se agregará a la carpeta `docs/`.

## Equipo

| Integrante | Responsabilidad principal |
|---|---|
| Vicente Machaca Kandy Jennyfer | Líder de proyecto, investigación, backend API REST |
| Pilco Caceres Shiomara Janeth | Base de datos, modelo entidad-relación, scripts DDL, seguridad |
| Mamani Canaza Mirian Nicol | Diseño UI/UX, prototipo en Stitch, frontend Vue 3, accesibilidad |

## Cómo colaborar

Lee [CONTRIBUTING.md](CONTRIBUTING.md): ramas, commits y Pull Requests.

## Licencia

- Código: [MIT](LICENSE).
- Documentación: Creative Commons BY-NC-SA 4.0.
- Datos agregados y anonimizados: dominio público.

Las librerías de terceros conservan sus propias licencias (Laravel, Vue, Tailwind CSS: MIT; PostgreSQL: licencia PostgreSQL; Inter y JetBrains Mono: SIL OFL 1.1).
