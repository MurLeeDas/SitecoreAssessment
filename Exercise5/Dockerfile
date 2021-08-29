FROM httpd:alpine3.14

RUN  apk update && apk upgrade && \
     apk add apache2 && \
     apk add apache2-proxy && \
     apk add apache2-ssl && \
     rm -rf /var/cache/apk/*

COPY conf.d/* /etc/apache2/
COPY config.json /etc/ui/config.json

CMD  [ "/usr/sbin/httpd", "-D", "FOREGROUND"]