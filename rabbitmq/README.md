# Redis

Sample docker-compose for RabbitMQ.

## Docker Compose

```yaml
version: '3'

services:
  rabbitmq:
    container_name: rabbitmq
    image: rabbitmq:3-management-alpine
    restart: always
    ports:
      - "15672:15672"
      - "5672:5672"

```

Once the container is running, the rabbitmq should be accessible through `localhost:15672`.
