FROM php:7.3-fpm

LABEL maintainer="NorthernBytes Ab Oy <contact@nbts.fi>"

RUN \
    apt-get update && \    
    apt-get install -y \
        libmcrypt-dev \
        libmagickwand-dev --no-install-recommends && \
    pecl install mcrypt-1.0.2 && \
    docker-php-ext-install pdo_mysql && \
    docker-php-ext-enable mcrypt

WORKDIR /var/www