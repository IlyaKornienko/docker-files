FROM ubuntu:latest

ENV TZ=Europe/Kyiv
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y \
    apache2 \
    php

RUN apt-get update && apt-get -y install software-properties-common && add-apt-repository ppa:ondrej/php && apt-get update && apt-get install -y \
    apache2 \
    php7.2 \
    libapache2-mod-php7.2 \
    php7.2-curl \
    php7.2-json 

RUN apt-get clean && rm -rf /var/lib/apt/lists/* && rm -rf /var/www/html/index.html

COPY ./index.php /var/www/html/index.php
CMD [ "apache2ctl", "-D", "FOREGROUND" ]
EXPOSE 80
