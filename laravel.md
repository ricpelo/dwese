# Crear un proyecto

composer create-project laravel/larevel proyecto
cd proyecto
configurar .env
npm install
npm run dev (o npm run watch)
php artisan migrate
php artisan serve

- Si queremos usar Breeze:

composer require laravel/breeze --dev
php artisan breeze:install
npm install
npm run dev
php artisan migrate

# Heroku

https://devcenter.heroku.com/articles/getting-started-with-laravel

- Crear el Procfile:

echo "web: vendor/bin/heroku-php-apache2 public/" > Procfile

- Activar el node.js:

heroku buildpacks:add heroku/nodejs

- Cambiar el package.json y crear una sección `dependencies` aparte de la `devDependencies`. Dejamos en `devDependencies` sólo el `postcss` y el `postcss-import` y movemos todo lo demás a `dependencies`:

{
    "private": true,
    "scripts": {
        "dev": "npm run development",
        "development": "mix",
        "watch": "mix watch",
        "watch-poll": "mix watch -- --watch-options-poll=1000",
        "hot": "mix watch --hot",
        "prod": "npm run production",
        "production": "mix --production"
    },
    "devDependencies": {
        "postcss": "^8.2.1",
        "postcss-import": "^14.0.1"
    },
    "dependencies": {
        "@tailwindcss/forms": "^0.4.0",
        "alpinejs": "^3.4.2",
        "autoprefixer": "^10.1.0",
        "axios": "^0.21",
        "laravel-mix": "^6.0.6",
        "lodash": "^4.17.19",
        "tailwindcss": "^3.0.0"
    }
}

- Configurar todos los APP_* y los DB_*

APP_NAME=Laravel
APP_ENV=production
APP_KEY=se genera con php artisan key:generate --show
APP_DEBUG=false
APP_URL=la URL base de la aplicación en Heroku, con https y sin / final

ASSET_URL=igual que APP_URL

- Configurar el error log, cambiando en config/logging.php:

<?php
return [
    'default' => env('LOG_CHANNEL', 'stack'),
    'channels' => [
        'stack' => [
            'driver' => 'stack',
            'channels' => ['single'],
        ],
        'single' => [
            'driver' => 'errorlog',
            'level' => 'debug',
        ],
…

- Instalar las Heroku CLI:

curl https://cli-assets.heroku.com/install-ubuntu.sh | sh

- Iniciar sesión:

heroku login

- Crear la base de datos

heroku addons:create heroku-postgresql:hobby-dev

- Arrancar las migraciones

heroku run php artisan migrate

- Hacer que las sesiones se almacenen en la base de datos:

SESSION_DRIVER=database

php artisan session:table
php artisan migrate

