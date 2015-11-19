# kafka-test
simple kafka test
http://sookocheff.com/post/kafka/kafka-quick-start/

## run docker container

````
docker-compose up -d
```

## testing kafka

### install kafkacat

e.g. use homebrew on osx `brew install kafkacat`

start 2 shells. One will be the producer / other the consumer

### Producer

```
kafkacat -P -b $(docker-machine ip default):9092 -t test 
Kafka
quick
start
guide.
```

### Consumer

```
kafkacat -C -b $(docker-machine ip default):9092 -t test
```
which should display the statements from above
