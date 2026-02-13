# SerraInnova - Inmobiliaria Sostenible

![Laravel](https://img.shields.io/badge/Laravel-12.0-FF2D20?style=flat&logo=laravel&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-3.0-4FC08D?style=flat&logo=vue.js&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.0-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.0-646CFF?style=flat&logo=vite&logoColor=white)

**SerraInnova** es una plataforma inmobiliaria diseñada para modernizar el mercado de viviendas sostenibles. Permite la gestión, búsqueda y análisis de propiedades basándose en su eficiencia energética y huella de carbono.

---

## � Características Principales

- **Buscador de Propiedades**: Filtrado por certificación energética (A-G) y tipo de energía renovable.
- **Calculadora de Huella de Carbono**: Herramienta interactiva para estimar emisiones y ahorro energético.
- **Blog Educativo**: Artículos sobre sostenibilidad, normativas y consejos de eficiencia.
- **Panel de Administración**: Gestión completa de propiedades y contenidos.

---

## 🛠️ Tecnologías Utilizadas

Este proyecto utiliza una arquitectura moderna separando el Backend del Frontend:

- **Backend**: Laravel 12 (API RESTful)
- **Frontend**: Vue.js 3 + Pinia (SPA)
- **Estilos**: Tailwind CSS 4
- **Base de Datos**: MySQL / SQLite

---

## ⚙️ Instalación

Sigue estos pasos para ejecutar el proyecto en tu ordenador:

### 1. Clonar el repositorio

```bash
git clone https://github.com/fardatxo/ProyectoPiieGrupo3.git
cd ProyectoPiieGrupo3
```

### 2. Instalar dependencias

Necesitarás dos terminales:

**En la Terminal 1 (Backend):**

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
php artisan storage:link
php artisan serve
```

**En la Terminal 2 (Frontend):**

```bash
npm install
npm run dev
```

La aplicación estará disponible en: `http://localhost:8000`

---

## 📂 Estructura del Proyecto

- `app/`: Lógica del servidor (Controladores, Modelos).
- `resources/js/`: Código del cliente (Vue.js, Componentes).
- `routes/`: Definición de rutas API y Web.
- `database/`: Migraciones y datos de ejemplo.

---

## 👥 Autores

Proyecto desarrollado por el **Grupo 3 PIIE**:

- **Adri** - [@fardatxo](https://github.com/fardatxo)
- **Gian** - [@GianCarlos25](https://github.com/GianCarlos25)
- **Alberto** - [@alarmi04](https://github.com/alarmi04)
- **Ismael** - [@pequemaquina-ctrl](https://github.com/pequemaquina-ctrl)
- **Alex** - [@AVL05](https://github.com/AVL05)

---

Licencia MIT.
