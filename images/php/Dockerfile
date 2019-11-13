FROM composer as vendor

COPY app/database/ database/
COPY app/composer.json composer.json
COPY app/composer.lock composer.lock

RUN composer install \
    --ignore-platform-reqs \
    --no-interaction \
    --no-plugins \
    --no-scripts \
    --prefer-dist \
    --no-dev



FROM php:7.2-fpm-alpine

RUN docker-php-ext-install mbstring tokenizer mysqli pdo_mysql

COPY app /var/www/html
COPY --from=vendor /app/vendor/ /var/www/html/vendor/
