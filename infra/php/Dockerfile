FROM php:8.1-fpm

RUN apt-get update && \
    apt-get -y install --no-install-recommends less git unzip libzip-dev libicu-dev libonig-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    docker-php-ext-install intl pdo_mysql zip bcmath

COPY ./src /data
COPY ./infra/php/www.conf /usr/local/etc/php-fpm.d/www.conf
