FROM php:7.4-apache

RUN apt-get update

RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable mysqli

RUN a2enmod rewrite

RUN apt-get install -y nano git

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 80
