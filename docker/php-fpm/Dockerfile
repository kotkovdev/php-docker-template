FROM php:7.4-fpm

RUN apt-get update && apt-get install -y wget unzip libpq-dev && pecl install xdebug && docker-php-ext-enable xdebug
RUN docker-php-ext-install pdo_pgsql

ADD ./php.ini /usr/local/etc/php/php.ini

RUN wget https://getcomposer.org/installer -O - -q \
    | php -- --install-dir=/bin --filename=composer --quiet

WORKDIR /var/www
