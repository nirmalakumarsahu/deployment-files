FROM php:8.2-fpm-alpine

LABEL maintainer="yourname@example.com"

WORKDIR /var/www

RUN apk add --no-cache \
    php8-pdo php8-pdo_mysql \
    php8-mbstring php8-tokenizer php8-xml \
    php8-curl php8-openssl php8-bcmath php8-json \
    && docker-php-ext-install pdo_mysql

COPY . .

EXPOSE 9000

CMD ["php-fpm"]