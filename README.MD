# To be used for public spring-cloud-dataflow or spring-cloud-stream

## 1. Sources

## Gemfire Source using Rabbitmq messaging

## Gemfire CQ Source using Rabbitmq messaging

## Time Source using Rabbitmq messaging

```
java -jar time-source-rabbit-1.0.0.BUILD-SNAPSHOT.jar --server.port=7070 --spring.cloud.stream.bindings.output.destination=ticktock
```

## 2. Processors

### Flat2tuple Processor using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/spring-cloud-stream-processor-flat2tuple-0.0.1-SNAPSHOT.jar

## 3. Sinks

### Gemfire Sink using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/spring-cloud-stream-sink-gemfire-1.0.jar

```
java -jar spring-cloud-stream-sink-gemfire-1.0.jar --regionName=RegionRaw --json=true --keyExpression="payload.getField('uuid')"
```

### Stomp Sink using Rabbitmq messaging
https://rawgit.com/komushi/spring-cloud-stream/master/spring-cloud-stream-sink-stomp-0.0.1-SNAPSHOT.jar