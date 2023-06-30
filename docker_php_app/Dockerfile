FROM ubuntu:latest

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y \
    apache2 \
    php

COPY ./index.php /var/www/html/index.php
CMD [ "/usr/sbin/httpd", "-D", "FOREGROUND" ]
EXPOSE 80