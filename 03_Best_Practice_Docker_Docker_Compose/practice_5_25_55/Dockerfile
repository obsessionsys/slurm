FROM alpine

RUN apk add --no-cache nginx && mkdir -p /run/nginx 

EXPOSE 80

COPY custom.conf /etc/nginx/conf.d/

COPY . /opt/

CMD ["nginx", "-g", "daemon off;"]