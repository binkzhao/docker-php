FROM nginx:alpine

MAINTAINER Mahmoud Zalt <mahmoud@zalt.me>

ADD nginx.conf /etc/nginx/

ARG PHP_UPSTREAM_CONTAINER=php-fpm
ARG PHP_UPSTREAM_PORT=9000

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data

# Set upstream conf and remove the default conf
RUN echo "upstream php-upstream { server ${PHP_UPSTREAM_CONTAINER}:${PHP_UPSTREAM_PORT}; }" > /etc/nginx/conf.d/upstream.conf \
    && rm /etc/nginx/conf.d/default.conf

ARG PHP_UPSTREAM_CONTAINER56=php-fpm56
ARG PHP_UPSTREAM_PORT56=9000
RUN echo "upstream php-upstream56 { server ${PHP_UPSTREAM_CONTAINER56}:${PHP_UPSTREAM_PORT56}; }" > /etc/nginx/conf.d/upstream56.conf

CMD ["nginx"]

EXPOSE 80 443
