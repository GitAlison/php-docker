FROM php:7.2-fpm-alpine

RUN docker-php-ext-install pdo pdo_mysql

# RUN apk add autoconf

RUN apk add --no-cache $PHPIZE_DEPS \
	&& pecl install xdebug-3.1.6 \
	&& docker-php-ext-enable xdebug

# RUN pecl install xdebug-3.1.6 \
# && docker-php-ext-enable xdebug

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

COPY ./app .