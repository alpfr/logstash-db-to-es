ARG ELASTIC_VERSION=8.15.0
FROM docker.elastic.co/logstash/logstash:${ELASTIC_VERSION}

WORKDIR /usr/share/logstash

# Copy main Logstash config and pipeline
COPY config/logstash.yml /usr/share/logstash/config/logstash.yml
COPY pipeline/db_to_es.conf /usr/share/logstash/pipeline/db_to_es.conf

# Copy PostgreSQL JDBC driver
COPY drivers/postgresql-42.7.3.jar /usr/share/logstash/logstash-core/lib/jars/postgresql-42.7.3.jar

# Default entrypoint/cmd from base image is fine
