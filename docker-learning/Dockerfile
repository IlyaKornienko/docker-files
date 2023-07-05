FROM ubuntu:16.04
LABEL maintainer="ilya94732@gmail.com"
ENV ADMIN="ilya"
RUN apt-get -y update && \
    apt-get -y install apache2

RUN echo 'Hello World from Docker!' > /var/www/html/index.html


CMD ["/usr/sbin/apache2ctl", "-D","FOREGROUND"]
EXPOSE 80

