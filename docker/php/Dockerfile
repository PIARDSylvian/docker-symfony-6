
FROM php:fpm-alpine3.14

# for mysql
# RUN apk --update --no-cache add git
# RUN docker-php-ext-install pdo_mysql for mysql

# for pgsql
RUN apk --update --no-cache add git postgresql-dev
RUN docker-php-ext-install pdo pdo_pgsql

COPY --from=composer /usr/bin/composer /usr/bin/composer
WORKDIR /var/www
CMD composer install; php-fpm;
EXPOSE 9000