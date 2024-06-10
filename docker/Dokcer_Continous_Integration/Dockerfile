FROM jenkins/jenkins
LABEL maintainer="munimdevops1111@gmail.com"
ENV REFRESHED_AT 2024_05_25

USER root

# Add retry logic for apt-get update
RUN apt-get -qqy update && \
    apt-get install -qqy sudo wget

# Configure sudo for Jenkins user
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

# Install Docker CLI
RUN wget http://get.docker.com/builds/Linux/x86_64/docker-latest.tgz && \
    tar -xvzf docker-latest.tgz && \
    mv docker/* /usr/bin/ && \
    rm -rf docker-latest.tgz docker

USER jenkins

# Install Jenkins plugins
# RUN /usr/local/bin/install-plugins.sh junit git git-client ssh-slaves greenballs chucknorris ws-cleanup
RUN jenkins-plugin-cli --plugins junit git git-client ssh-slaves greenballs chucknorris ws-cleanup
