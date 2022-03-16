# Kafka & Zookeeper

Sample docker-compose for running kafka with zookeeper.

## Docker Compose

In this samples, there are 6 setup in running kafka with zookeeper:
* [Single zookeeper and single kafka](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/zk-single-kafka-single.yml)
* [Single zookeeper and multiple kafka](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/zk-single-kafka-multiple.yml)
* [Multiple zookeeper and single kafka](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/zk-multiple-kafka-single.yml)
* [Multiple zookeeper and multiple kafka](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/zk-multiple-kafka-multiple.yml)
* [Multiple zookeeper and multiple kafka with schema registry](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/zk-multiple-kafka-multiple-schema-registry.yml)
* [Kafka fullstack](https://github.com/abiwinanda/docker-compose-collections/blob/master/kafka-zookeeper/kafka-full-stack.yml)

To run the specific docker compose file you could run

```sh
docker-compose -f [DOCKER_COMPOSE_FILE] up -d
```
