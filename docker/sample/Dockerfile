FROM ubuntu:18.04
LABEL maintainer="munimdevops1111@gmail.com"
ENV REFRESHED_AT 2024_05_21
RUN apt-get -yqq update; apt-get -yqq install nginx
RUN mkdir -p /var/www/html/website
ADD global.conf /etc/nginx/conf.d/
ADD nginx.conf /etc/nginx/nginx.conf
EXPOSE 80