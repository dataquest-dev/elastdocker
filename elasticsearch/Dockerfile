ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# create backup directory
RUN mkdir /home/backup && \
    chown -R elasticsearch:root /home/backup


# Add healthcheck
HEALTHCHECK CMD sh ./docker-healthcheck