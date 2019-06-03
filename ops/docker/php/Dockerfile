FROM php:7.3.3-fpm-alpine3.8

LABEL maintainer="eden.reich@gmail.com"

ARG XDEBUG_VERSION=2.7.0
ARG INSTALL_XDEBUG=false
ARG APP_ENV=local

ENV COMPOSER_ALLOW_SUPERUSER=1

COPY config/base.ini /usr/local/etc/php/conf.d/base.ini
COPY config/${APP_ENV}.ini /usr/local/etc/php/conf.d/${APP_ENV}.ini

RUN apk add --no-cache --update composer nodejs nodejs-npm

RUN docker-php-ext-install pdo_mysql

RUN \
if [ ${INSTALL_XDEBUG} = true ]; then \
    apk add --no-cache --virtual .build-deps $PHPIZE_DEPS && \
    pecl install xdebug-${XDEBUG_VERSION} && docker-php-ext-enable xdebug && \
    apk del .build-deps; \
fi

VOLUME /code

WORKDIR /code

EXPOSE 9000