# Base Image 
FROM ubuntu:16.04

MAINTAINER Amit Vashist <amitvashist7@outlook.com>

RUN apt-get update 

RUN apt-get install apache2 -y

COPY ports.conf /etc/apache2/

COPY index.html /var/www/html/

EXPOSE 8081 

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"] 
