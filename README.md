<h1 align="center">🌬️ Laravel + Tailwind CSS Starter</h1>

<p align="center">
  A minimal Laravel 10 boilerplate with Tailwind CSS 3 wired through Vite 4 –<br>
  clone it to skip the asset-pipeline setup on your next project.
</p>

<p align="center">
  <a href="#-quick-start">🚀 Quick Start</a> •
  <a href="#-scripts">📦 Scripts</a> •
  <a href="#-structure">🏗️ Structure</a> •
  <a href="#-configuration">⚙️ Configuration</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Laravel-10-FF2D20?logo=laravel&logoColor=white" alt="Laravel 10">
  <img src="https://img.shields.io/badge/PHP-8.1%2B-777BB4?logo=php&logoColor=white" alt="PHP 8.1">
  <img src="https://img.shields.io/badge/Tailwind-3-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS 3">
  <img src="https://img.shields.io/badge/Vite-4-646CFF?logo=vite&logoColor=white" alt="Vite 4">
</p>

---

## 🌟 Highlights

- 🎨 **Tailwind CSS 3** loaded as a PostCSS plugin directly inside `vite.config.js` (plus `autoprefixer`)
- 📁 **Predictable output** – Vite writes to `public/assets/{css,js}` with stable file names (`js/app.js`, `css/app.css`) and a `manifest.json`, so the compiled assets can be committed and served without a build step on the server
- 🔐 **Sanctum**, **Pint**, **Sail** and **PHPUnit 10** come with the Laravel 10 skeleton
- 🌓 Default welcome page already uses Tailwind utility classes with dark-mode variants

## ✨ What's inside

The stock Laravel 10.12 skeleton (`/` → `welcome.blade.php`, `User` model, four default migrations) plus:

- `tailwind.config.js` scanning `resources/**/*.{blade.php,js,vue}`
- `resources/css/app.css` importing Tailwind's base/components/utilities layers
- A customised `vite.config.js` (`outDir: public/assets`, `manifest: true`, fixed entry/chunk/asset names)
- Pre-built assets in `public/assets/` (committed)

## 🚀 Quick Start

```bash
composer install
cp .env.example .env
php artisan key:generate
npm install
npm run build      # or npm run dev for HMR
php artisan serve  # http://localhost:8000
```

## 📦 Scripts

| Script          | Description                                   |
| --------------- | --------------------------------------------- |
| `npm run dev`   | Vite dev server with HMR                      |
| `npm run build` | Production build to `public/assets`           |

## 🏗️ Structure

```
.
├── app/                  # Laravel 10 skeleton (Models/User.php, Http, Providers…)
├── config/
├── database/             # factories, migrations, seeders
├── public/
│   └── assets/           # Vite output: css/app.css, js/app.js, manifest.json
├── resources/
│   ├── css/app.css       # Tailwind layers
│   ├── js/app.js, bootstrap.js
│   └── views/welcome.blade.php
├── routes/
├── tests/                # Feature/ExampleTest, Unit/ExampleTest
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```

## ⚙️ Configuration

Environment variables (from `.env.example`): `APP_NAME`, `APP_ENV`, `APP_KEY`, `APP_DEBUG`, `APP_URL`, `LOG_*`, `DB_*`, `BROADCAST_DRIVER`, `CACHE_DRIVER`, `FILESYSTEM_DISK`, `QUEUE_CONNECTION`, `SESSION_*`, `MEMCACHED_HOST`, `REDIS_*`, `MAIL_*`, `AWS_*`, `PUSHER_*`, `VITE_PUSHER_*`.

The welcome view links the compiled stylesheet directly (`<link href="assets/css/app.css">`) instead of using the `@vite` directive; if you switch to `@vite`, point it at the custom output directory with `Vite::useBuildDirectory('assets')` or remove the `build` block in `vite.config.js` to return to the default `public/build`.

## 🚀 Deployment

Standard Laravel: web root at `public/`, `composer install --no-dev --optimize-autoloader`, `php artisan migrate --force`, `npm run build` (or deploy the committed `public/assets`), then `php artisan optimize`.

## 🧪 Testing

```bash
php artisan test
```

## 📄 License

No license has been chosen yet.

## 👤 Author

**Chalii wa UX/UI** – [@chaliiwaui](https://github.com/chaliiwaui)

- 📧 Email: me@makindajackson.com
- 💼 LinkedIn: [Jackson Makinda](https://linkedin.com/in/makindajack)
- 🎨 Dribbble: [@makindajack](https://dribbble.com/makindajack)
- 🐦 Twitter: [@makindajack](https://twitter.com/makindajack)

---

Built with ❤️ in Dar es Salaam, Tanzania 🇹🇿
