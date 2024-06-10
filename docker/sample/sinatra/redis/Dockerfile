FROM ubuntu:18.04
LABEL maintainer="munimdevops1111@gmail.com"
ENV REFRESHED_AT 2024_05_25
RUN apt-get -yqq update && \
    apt-get -yqq install redis-server redis-tools
EXPOSE 6379
ENTRYPOINT [ "/usr/bin/redis-server" ]
CMD [ ]