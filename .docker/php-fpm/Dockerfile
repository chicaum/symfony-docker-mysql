FROM php:7.2-fpm

RUN apt-get update && apt-get install -y
RUN pecl install xdebug-2.6.1 \
     && docker-php-ext-enable xdebug
RUN apt install -y libicu-dev
RUN docker-php-ext-install -j$(nproc) intl
RUN apt install -y mysql-client
RUN docker-php-ext-install pdo_mysql
