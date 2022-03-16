# Postgresql

Sample docker-compose for Postgis.

## Docker Compose

```yaml
version: '3'

services:
  postgis:
    container_name: postgis
    image: kartoza/postgis:12.0
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
      PGDATA: /var/lib/postgresql/data/pgdata
    restart: always
    ports:
      - "5432:5432"

```

Once the container is running, the postgis should be accessible through `localhost:5432`.
