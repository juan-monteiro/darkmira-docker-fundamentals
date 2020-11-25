FROM php:fpm-alpine

RUN apk --update --no-cache add icu-dev libzip-dev \
 && docker-php-ext-install intl zip