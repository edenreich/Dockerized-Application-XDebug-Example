FROM nginx:alpine

LABEL maintainer="eden.reich@gmail.com"

RUN addgroup -g 1000 -S www-data \
 && adduser -u 1000 -D -S -G www-data www-data

COPY config/nginx.conf /etc/nginx/nginx.conf

COPY config/site.conf /etc/nginx/conf.d/default.conf

WORKDIR /etc/nginx

EXPOSE 80