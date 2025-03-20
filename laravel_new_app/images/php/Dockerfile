# 8.3.14-fpm-alpine

FROM php:8.3.14-fpm-alpine

# instalação de dependências 
RUN apk update && apk add --no-cache \ 
    libpng-dev \
    libjpeg-turbo-dev \
    freetype-dev \
    libzip-dev \
    git \
    unzip \
    icu-dev \
    libxml2-dev \
    openssl-dev \
    bash \
    --virtual .build-deps gcc g++ make

#Instalar extensão PDO MySQL
RUN docker-php-ext-install gd pdo pdo_mysql

# Instalar o NodeJS
RUN apk add nodejs npm 
RUN apk upgrade

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer