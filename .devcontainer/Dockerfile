FROM php:7.4-apache

RUN apt-get update

# Instala as extensões do MySQL e intl
RUN docker-php-ext-install mysqli pdo pdo_mysql intl
RUN docker-php-ext-enable mysqli

# Ative o mod_rewrite para o Apache
RUN a2enmod rewrite

# Instala o nano (editor de texto) e o git
RUN apt-get install -y nano git

# Instala o Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 80
