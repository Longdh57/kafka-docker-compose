# Kafka with Python
This project created for practice Kafka system and run demo project running on Python
![kafka_icon.png](kafka_icon.png)

## Initial Kafka
Run docker-compose with
```
$ docker-compose up -d

$ docker exec -it kafka bash
```

# Some Kafka cli
## Topic
```
## Create a topic
$ kafka-topics.sh \
    --bootstrap-server localhost:9092 \
    --topic my-first-topic \
    --create \
    --partitions 3 \
    --replication-factor 1

## List all
$ kafka-topics.sh \
    --bootstrap-server localhost:9092 \
    --list
    
## Describe
$ kafka-topics.sh \
    --bootstrap-server localhost:9092 \
    --topic my-first-topic \
    --describe
    
## Delete
$ kafka-topics.sh \
    --bootstrap-server localhost:9092 \
    --topic my-first-topic \
    --delete
```
## Producer
```
## Create a Producer
$ kafka-console-producer.sh \
    --bootstrap-server localhost:9092 \
    --topic my-first-topic  # After that input and Enter to make message
>


```

## Consumer
```
## Initial a kafka consumer & get message from beginning
$ kafka-console-consumer.sh \
--bootstrap-server localhost:9092 \
--topic my-first-topic \
--from-beginning

## Initial a kafka consumer groups
$ kafka-console-consumer.sh     \
--bootstrap-server localhost:9092 \
--topic my-first-topic \
--group my-first-app

## List Consumer Groups
$ kafka-consumer-groups.sh \
    --bootstrap-server localhost:9092 \
    --list
```

# Python with Kafka
## Producer
Run file initial Producer and initial consumer/consumer-groups from kafka cli to check
`$ python kafka_producer.py`


## Consumer
Run Consumer and Producer in same time
```
$ python kafka_consumer.py

$ python kafka_producer.py
```