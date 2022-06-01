ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}
ENV DEBIAN_FRONTEND=noninteractive

# create backup directory
RUN mkdir /home/backup && \
    chown -R elasticsearch:root /home/backup

# install PRE-REQUISITES + ELASTICDUMP
RUN apt-get update
RUN apt-get -y install curl gnupg
RUN curl -sL https://deb.nodesource.com/setup_16.x  | bash -
RUN apt-get -y install nodejs
RUN npm install -g elasticdump

# Add healthcheck
HEALTHCHECK CMD sh ./docker-healthcheck