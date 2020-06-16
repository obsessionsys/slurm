FROM alpine

COPY . /opt/

RUN apk add --no-cache nginx && mkdir -p /run/nginx 

COPY custom.conf /etc/nginx/conf.d/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]