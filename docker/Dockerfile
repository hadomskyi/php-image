FROM php:7.4

RUN apt-get update -yqq
RUN apt-get install -y unzip git libbz2-dev
RUN pecl install redis
RUN docker-php-ext-enable redis
RUN docker-php-ext-install pdo_mysql bcmath bz2
