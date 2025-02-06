# Todo App Fullstack

Este repositorio contiene una aplicación fullstack de tareas (TODO App), donde se incluye tanto el frontend (todo-app) como la API (todo-api).

## Estructura del Proyecto

- **todo-app**: El frontend de la aplicación, desarrollado con vuejs [repositorio](https://github.com/LiReyes/todo-app).
- **todo-api**: El backend que maneja la lógica de negocio y las bases de datos de la aplicación, desarrollado con laravel [repositorio](https://github.com/LiReyes/todo-api).


## Requisitos previos

Asegúrate de tener instalados los siguientes componentes:

- [Docker](https://www.docker.com/products/docker-desktop) para ejecutar el contenedor de MariaDB.
- [PHP](https://www.php.net/downloads.php) (recomendado PHP 8.2).
- [Composer](https://getcomposer.org/) para gestionar las dependencias de PHP.
- [Laravel](https://laravel.com/docs/9.x) (si se quiere usar el CLI de Laravel).
- [Node.js](https://nodejs.org/) (correr app de vue)

## Detalles

Para mayor detalle al inicializar el proyecto consultar ambos repositorios donde se explica mas el como usarlo y su respectiva instalacion:

- FRONTEND: [todo-app](https://github.com/LiReyes/todo-app).

- BACKEND + BD: [todo-api](https://github.com/LiReyes/todo-api).

## Configuración rapida

1. Levantar mariaDB con docker
```bash
docker compose up
```
2. Instalar dependencias de PHP
```bash
composer install
composer update
```
3. Copiar .env.example 
```bash
DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=todo-db
DB_USERNAME=root
DB_PASSWORD=root
```

4. Ejecutar migraciones + seeders
```bash
php artisan migrate:refresh --seed
```

5. Levantar la APIRest
```bash
php artisan serve
```
inicia:
```bash
API URL = http://127.0.0.1:8000 o http://localhost:8000
```

6. Verificar instalacion de node

```sh
node -v
npm -v
```

7. Crea un archivo `.env` en la raíz del proyecto y agrega la siguiente variable de entorno para apuntar a tu API local:

```sh
VITE_API_URL=http://localhost:8000
```


8. Instalación de dependencias:
```sh
npm install
```

9. Ejecutar el proyecto:

```sh
npm run dev
```