# Employee Manager — Docker

Aplicación web de gestión de empleados multicontenedor desplegada con Docker Compose.

## Tecnologías

- **Frontend**: HTML + CSS + JavaScript, servido por Nginx
- **Backend**: Node.js + Express (API REST)
- **Base de datos**: PostgreSQL 15 (persistente con volumen Docker)

## Funcionalidades

- Crear, editar y eliminar empleados
- Campos: nombre, email, departamento, cargo y salario
- Panel de estadísticas en tiempo real (total empleados, departamentos, salario medio)

## Requisitos

- Docker
- Docker Compose

## Arranque

```bash
./start.sh
```

La aplicación estará disponible en `http://localhost` (puerto 80).

## Estructura

```
├── backend/
│   ├── src/
│   │   ├── index.js          # Entrada de la aplicación
│   │   ├── db.js             # Conexión y configuración de la DB
│   │   └── routes/
│   │       └── employees.js  # Rutas CRUD
│   ├── package.json
│   └── Dockerfile
├── frontend/
│   ├── src/
│   │   ├── index.html
│   │   ├── css/style.css
│   │   └── js/app.js
│   ├── nginx.conf
│   └── Dockerfile
├── docker-compose.yml
└── start.sh
```