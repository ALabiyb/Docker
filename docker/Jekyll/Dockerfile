FROM ubuntu:20.04
LABEL maintainer="munimdevops1111@gmail.com"
ENV REFRESHED_AT 20240530

RUN apt-get -yqq update && \
    apt-get -yqq install ruby ruby-dev build-essential nodejs

RUN gem install jekyll -v 2.5.3

VOLUME /data
VOLUME /var/www/html
WORKDIR /data

ENTRYPOINT [ "jekyll", "build", "--destination=/var/www/html" ]

