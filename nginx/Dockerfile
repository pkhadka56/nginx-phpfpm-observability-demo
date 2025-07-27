FROM nginx:1.29.0-alpine3.22

RUN adduser -S www-data -G nginx

RUN mkdir -p /var/cache/nginx/client_temp /var/log/nginx/ /var/www/html \
    && chown -R www-data:nginx /var/cache/nginx /var/log/nginx/ /var/www/html

COPY nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf
COPY nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./app/ /var/www/html/

WORKDIR /var/www/html

EXPOSE 8080

USER www-data
