# To be used for public spring-cloud-dataflow or spring-cloud-stream

## 1. Sources

## Gemfire Source using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/gemfire-source-rabbit-1.0.0.BUILD-SNAPSHOT.jar

## Gemfire CQ Source using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/gemfire-cq-source-rabbit-1.0.0.BUILD-SNAPSHOT.jar

## Time Source using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/time-source-rabbit-1.0.0.BUILD-SNAPSHOT.jar

```
java -jar time-source-rabbit-1.0.0.BUILD-SNAPSHOT.jar --server.port=7070 --spring.cloud.stream.bindings.output.destination=ticktock
```

## 2. Processors

### Flat2tuple Processor using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/Flat2TupleTransformer-0.0.1-SNAPSHOT.jar

## 3. Sinks

### Gemfire Sink using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/gemfire-sink-rabbit-1.0.0.BUILD-SNAPSHOT.jar

```
java -jar gemfire-sink-rabbit-1.0.0.BUILD-SNAPSHOT.jar --regionName=RegionRaw --json=true --keyExpression="payload.getField('uuid')"
```

### Websocket Sink using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/websocket-sink-rabbit-1.0.0.BUILD-SNAPSHOT.jar