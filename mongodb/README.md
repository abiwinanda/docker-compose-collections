# MongoDB

MongoDB sample docker-compose. 

## Docker Compose

```yaml
version: "3.9"

services:

  mongo:
    image: mongo
    ports:
      - 27017:27017
    restart: always
    environment:
      MONGO_INITDB_ROOT_USERNAME: root
      MONGO_INITDB_ROOT_PASSWORD: password

```

Once the container is running, the MongoDB should be accessible through `localhost:27017`.
