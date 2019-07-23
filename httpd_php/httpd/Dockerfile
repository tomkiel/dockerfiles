FROM php:7.2-apache

ARG WEB_USER
ARG WEB_GROUP
ARG APACHE_ROOT_DIR

RUN apt update && apt install -y libpq-dev && docker-php-ext-install pdo pdo_pgsql
RUN usermod -u 1000 ${WEB_USER} \
 && groupmod -g 1000 ${WEB_GROUP} \
 && chgrp -R ${WEB_GROUP} /var/www/html
