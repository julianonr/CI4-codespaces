FROM php:7.4-apache

# Atualiza os pacotes
RUN apt-get update

# Instala as dependências necessárias
RUN apt-get install -y libicu-dev git nano unzip libzip-dev

# Instala as extensões PHP
RUN docker-php-ext-configure intl
RUN docker-php-ext-configure zip
RUN docker-php-ext-install mysqli pdo pdo_mysql intl zip
RUN docker-php-ext-enable mysqli

# Ative o mod_rewrite para o Apache
RUN a2enmod rewrite

# Instala o Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 80
