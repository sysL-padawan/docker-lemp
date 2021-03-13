ARG php_version

FROM php:${php_version}-fpm-alpine

RUN docker-php-ext-install mysqli && \
    docker-php-ext-install pdo_mysql