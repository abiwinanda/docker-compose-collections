# Elasticsearch with Kibana

Sample docker-compose for Elasticsearch with Kibana.

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

  kibana:
    container_name: kibana
    image: docker.elastic.co/kibana/kibana:7.4.2
    environment:
      - xpack.security.enabled=false
      - ELASTICSEARCH_HOSTS=http://elasticsearch:9200
    depends_on:
      - elasticsearch
    ports:
      - 5601:5601

```

Once the container is running, the kibana should be accessible through `localhost:5601`.

## Common Issues

### Kibana Server Not Ready

When you try to access kibana after its initial container spin up you might get `Kibana server is not ready yet` error. It takes some time for the Kibana to be ready hence you could keep refreshing the page request until success.
