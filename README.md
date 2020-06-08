## Project Overview

This is a simple setup for using docker with laravel.

It includes nginx, mysql and redis.

## How to use

run `cp .env.example .env`

set the following .env variables:

* DB_PORT=database
* DB_DATABASE=laravel
* DB_USERNAME=root
* DB_PASSWORD=secret

if using redis add these variables:

* CACHE_DRIVER=redis
* REDIS_HOST=redis

run `composer install`

run `sudo chmod 777 storage/ -R`

run `docker-compose exec php php artisan key:generate`

run `docker-compose exec php php artisan migrate`

run `docker-compose up -d`
