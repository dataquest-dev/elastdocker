ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

RUN echo "hopefully running"

# Add healthcheck
COPY elasticsearch/scripts/docker-healthcheck .
HEALTHCHECK CMD sh ./docker-healthcheck