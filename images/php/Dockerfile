FROM php:7.3-fpm-alpine
RUN apk add --no-cache libzip-dev && docker-php-ext-configure zip --with-libzip=/usr/include && docker-php-ext-install zip
RUN docker-php-ext-install mbstring tokenizer mysqli pdo_mysql
COPY --from=composer /usr/bin/composer /usr/bin/composer
RUN composer global require "laravel/lumen-installer"
# uncomment the line below if creating a new project
# RUN composer create-project --prefer-dist laravel/lumen ilib_api
