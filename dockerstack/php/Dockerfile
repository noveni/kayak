FROM php:7.2-fpm
RUN apt-get update && apt-get install -y \
                                apt-utils \
                                libbz2-dev \
                                libssl-dev
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install bz2
RUN docker-php-ext-install calendar
RUN docker-php-ext-install dba
RUN docker-php-ext-install exif
RUN docker-php-ext-install ftp

RUN docker-php-ext-install mysqli
RUN apt-get install -y libpq-dev
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install pdo_pgsql

RUN apt-get update && apt-get install -y zlib1g-dev
RUN docker-php-ext-install zip

RUN docker-php-ext-install mbstring

WORKDIR /var/www/
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer