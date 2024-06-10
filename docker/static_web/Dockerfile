# Version: 0.0.1
FROM ubuntu:18.0.4
LABEL maintainer="munimdevops1111@gmail.com"
RUN apt-get update; apt-get install -y ngnix
RUN echo 'Hi, I am in your container' \
    >/var/www/html/index.html
EXPOSE 80