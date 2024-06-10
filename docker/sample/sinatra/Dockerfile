FROM ubuntu:18.04

LABEL maintainer="munim@example.com"

ENV REFRESHED_AT 2024-05-25

# Install necessary dependencies for Ruby installation
RUN apt-get update -yqq && apt-get install -yqq software-properties-common

# Add PPA for a newer Ruby version
RUN apt-add-repository ppa:brightbox/ruby-ng

# Update and install Ruby 2.7
RUN apt-get update -yqq && apt-get install -yqq ruby2.7 ruby2.7-dev build-essential redis-tools

# Update alternatives to use Ruby 2.7 by default
RUN update-alternatives --install /usr/bin/ruby ruby /usr/bin/ruby2.7 1 && \
    update-alternatives --install /usr/bin/gem gem /usr/bin/gem2.7 1

# Install specific versions of gems without documentation
RUN gem install --no-document 'sinatra:2.1.0' 'json' 'redis:4.1.4'  

RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD [ "/opt/webapp/bin/webapp" ]