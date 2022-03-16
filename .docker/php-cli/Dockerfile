FROM php:8.1.0-cli-alpine3.14

RUN apk update && apk upgrade
RUN apk add --no-cache bash
RUN apk add make zip libzip-dev gnupg

RUN docker-php-ext-install zip pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
