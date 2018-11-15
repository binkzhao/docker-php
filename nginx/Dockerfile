FROM blzhaobink/nginx:latest

MAINTAINER Bink Zhao <781270119@qq.com>

ADD nginx.conf /etc/nginx/

ARG PHP_UPSTREAM_CONTAINER=php-fpm
ARG PHP_UPSTREAM_PORT=9000

#RUN apk update \
#    && apk upgrade \
#    && apk add --no-cache bash \
#    && adduser -D -H -u 1000 -s /bin/bash www-data

# Set upstream conf and remove the default conf
RUN echo "upstream php-upstream { server ${PHP_UPSTREAM_CONTAINER}:${PHP_UPSTREAM_PORT}; }" > /etc/nginx/conf.d/upstream.conf \
    && if [ -e "/etc/nginx/conf.d/default.conf" ]; then rm /etc/nginx/conf.d/default.conf; fi

CMD ["nginx"]

EXPOSE 80 443
