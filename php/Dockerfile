FROM php:7.4-fpm
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
COPY ./php.ini /usr/local/etc/php/

RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev libonig-dev libzip-dev unzip locales git vim\
  && docker-php-ext-install pdo_mysql mysqli gd iconv exif zip bcmath