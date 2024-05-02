FROM php:7.2-fpm-alpine

RUN docker-php-ext-install pdo pdo_mysql

# ENV COMPOSER_ALLOW_SUPERUSER=1
# 2.1.8
# 2.7.4
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

COPY ./app .