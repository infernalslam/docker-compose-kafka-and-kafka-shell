## Frist step run docker-compose
```
### docker-compose -f docker-compose.yml up -d
```

```
cd kafka_2.11-2.0.0
$ bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic <test> // rename <test>
$ bin/kafka-topics.sh --list --zookeeper localhost:2181
```

## Send some messages
```
$ bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
```

## tart a consumer

```
$ bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
```

