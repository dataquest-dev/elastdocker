ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

RUN echo "still not running"
RUN sysctl --w vm.max_map_count=262144
# RUN echo -e "\nvm.max_map_count = 262144\n" >> /etc/sysctl.d/99-sysctl.conf

# Add healthcheck
COPY elasticsearch/scripts/docker-healthcheck .
HEALTHCHECK CMD sh ./docker-healthcheck