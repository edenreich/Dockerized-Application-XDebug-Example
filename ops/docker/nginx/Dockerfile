FROM nginx:alpine

LABEL maintainer="eden.reich@gmail.com"

COPY config/nginx.conf /etc/nginx/nginx.conf

COPY config/site.conf /etc/nginx/conf.d/default.conf

WORKDIR /etc/nginx

EXPOSE 80