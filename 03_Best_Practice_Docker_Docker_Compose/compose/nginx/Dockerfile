FROM alpine:3.11.5

ENV NGINX_VERSION 1.16.1-r6

RUN apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.11/main nginx=${NGINX_VERSION} \
 && mkdir -p /run/nginx
 #\
 ## If ipv6 is disabled on host
 #\
 #&& sed -i -e '/\[\:\:\]\:80/d' /etc/nginx/nginx.conf \
 #&& sed -i -e '/\[\:\:\]\:80/d' /etc/nginx/conf.d/default.conf

EXPOSE 80

COPY custom.conf /etc/nginx/conf.d/

COPY ./www/ /var/www/

CMD ["nginx", "-g", "daemon off;"]