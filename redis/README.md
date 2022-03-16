# Redis

Sample docker-compose for Redis.

## Docker Compose

```yaml
version: '3'

services:
  redis:
    container_name: redis
    image: redis:5.0-alpine
    restart: always
    ports:
      - "6379:6379"

```

Once the container is running, the redis should be accessible through `localhost:6379`.
