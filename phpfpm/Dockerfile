FROM php:8.4-fpm-alpine3.21

WORKDIR /var/www/html

RUN chown -R www-data:www-data /var/www/html

COPY ./app/ /var/www/html/

EXPOSE 9000

USER www-data
