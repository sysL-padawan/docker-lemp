ARG php_version

FROM php:${php_version}-fpm-alpine

RUN docker-php-ext-install mysqli && \
    docker-php-ext-install pdo_mysql && \
    apk add --no-cache $PHPIZE_DEPS  && \
    pecl install xdebug && \
    docker-php-ext-enable xdebug