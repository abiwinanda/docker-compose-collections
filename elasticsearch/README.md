# Elasticsearch

Sample docker-compose for Elasticsearch.

## Docker Compose

```yaml
version: '3'

services:
  elasticsearch:
    container_name: elasticsearch
    image: elasticsearch:7.4.2
    environment:
      - "discovery.type=single-node"
    restart: always
    ports:
      - "9200:9200"

```

Once the container is running, the elasticsearch should be accessible through `localhost:9200`.
