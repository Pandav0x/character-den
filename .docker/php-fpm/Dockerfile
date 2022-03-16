FROM php:8.1.0-fpm-alpine3.14

RUN apk update && apk upgrade
RUN apk add --no-cache bash
RUN apk add zip libzip-dev gnupg

RUN docker-php-ext-install zip pdo_mysql opcache

RUN apk add --no-cache $PHPIZE_DEPS 
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

COPY opcache.ini /usr/local/etc/php/conf.d/opcache.ini
COPY xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
