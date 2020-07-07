FROM php:7.4

RUN apt-get update -yqq
RUN apt-get install -y unzip git libbz2-dev
RUN pecl install redis
RUN docker-php-ext-enable redis
RUN docker-php-ext-install pdo pdo_mysql bcmath bz2

RUN apt-get update && apt-get install -y openssl git unzip libbz2-dev

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN curl --location --output /usr/local/bin/phpcpd https://phar.phpunit.de/phpcpd.phar
RUN curl --location --output /usr/local/bin/phpcs https://squizlabs.github.io/PHP_CodeSniffer/phpcs.phar

RUN chmod +x /usr/local/bin/composer
RUN chmod +x /usr/local/bin/phpcpd
RUN chmod +x /usr/local/bin/phpcs

RUN docker-php-ext-enable pdo
RUN docker-php-ext-enable pdo_mysql
RUN docker-php-ext-enable xdebug
RUN docker-php-ext-enable redis.so
RUN docker-php-ext-enable bcmath
RUN docker-php-ext-enable bz2