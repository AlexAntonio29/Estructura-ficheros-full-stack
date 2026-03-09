
# poc-app

Desarrollaras una aplicación web **fullstack** con frontend, backend y base de datos PostgreSQL orquestados con Docker Compose.

---

## 1. Descripción general

Este POC busca implementar un prototipo funcional con la siguiente arquitectura:

- Frontend (HTML/CSS/JS o framework) consumiendo una API REST.
- Backend en Node.js/Express exponiendo endpoints HTTP.
- Base de datos PostgreSQL con scripts de inicialización.
- Orquestación de servicios mediante Docker Compose.

---

## 2. Requisitos

Antes de empezar, asegúrate de tener instalado:

- Git
- Docker y Docker Compose
- Node.js (opcional, si quieres correr backend/frontend fuera de Docker)

---

## 3. Estructura del proyecto

La estructura final del proyecto será:


```bash
poc-app/
├── backend/
│   └── src/
│       ├── controllers/
│       │   └── example.controller.js
│       ├── models/
│       │   └── example.model.js
│       ├── routes/
│       │   └── index.js
│       ├── services/
│       │   ├── example.service.js
│       │   └── index.js
│       └── Dockerfile
├── db/
├── docs/
├── frontend/
│   └── src/
│       ├── assets/
│       ├── components/
│       │   └── Header.js
│       ├── pages/
│       │   └── index.html
│       ├── styles/
│       │   └── main.css
│       └── main.js
├── Dockerfile
├── .gitignore
├── docker-compose.yml
└── README.md
```

---

## Opción 1: Construcción paso a paso

```bash
# 1. Crear carpeta raíz y entrar
mkdir poc-app
cd poc-app

# 2. Crear carpetas principales
mkdir backend
mkdir frontend
mkdir db
mkdir docs

# 3. Crear estructura interna del backend
mkdir -p backend/src
mkdir -p backend/src/controllers
mkdir -p backend/src/models
mkdir -p backend/src/routes
mkdir -p backend/src/services

# 4. Crear archivos base del backend
touch backend/src/index.js
touch backend/src/controllers/example.controller.js
touch backend/src/models/example.model.js
touch backend/src/routes/index.js
touch backend/src/services/index.js
touch backend/src/services/example.service.js
touch backend/Dockerfile

# 5. Crear estructura interna del frontend
mkdir -p frontend/src
mkdir -p frontend/src/assets
mkdir -p frontend/src/components
mkdir -p frontend/src/pages
mkdir -p frontend/src/styles

# 6. Crear archivos base del frontend
touch frontend/src/main.js
touch frontend/src/components/Header.js
touch frontend/src/pages/index.html
touch frontend/src/styles/main.css
touch frontend/Dockerfile

# 7. Crear archivos raíz del proyecto
touch .gitignore
touch Dockerfile
touch docker-compose.yml
touch README.md
```

---

## Opción 2: Crear todo con pocas líneas

```bash
# Crear toda la estructura de directorios de una vez
mkdir -p poc-app/{backend/src/{controllers,models,routes,services},frontend/src/{assets,components,pages,styles},db,docs}

# Entrar al proyecto
cd poc-app

# Crear archivos base backend
touch backend/src/index.js \
      backend/src/controllers/example.controller.js \
      backend/src/models/example.model.js \
      backend/src/routes/index.js \
      backend/src/services/index.js \
      backend/src/services/example.service.js \
      backend/Dockerfile

# Crear archivos base frontend
touch frontend/src/main.js \
      frontend/src/components/Header.js \
      frontend/src/pages/index.html \
      frontend/src/styles/main.css \
      frontend/Dockerfile

# Crear archivos raíz del proyecto
touch .gitignore Dockerfile docker-compose.yml README.md
```

---

## Opción 3: Clonar el repositorio ya preparado

Si el profesor ya publicó este proyecto como plantilla en GitHub:

```bash
# 1. Clonar el repositorio
git clone https://github.com/USUARIO/poc-app.git

# 2. Entrar a la carpeta del proyecto
cd poc-app

# 3. (Opcional) Verificar la estructura
tree -L 3
```

> Sustituye `USUARIO` por el nombre de la cuenta o la organización donde esté alojado el repositorio.

---

## Próximos 