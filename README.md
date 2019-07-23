# jaeger-tracing-kafka

![alt text](jaeger-tracing-kafka.png)

This is an example of a Kafka project with Jaeger tracing.

# Instructions
Execute `docker-compose up -d`

After everything comes up, execute:
```
cd ./kafka-connect/file-source
curl -X POST -H "Content-Type: application/json" --data @file-source.json http://localhost:8083/connectors
curl http://localhost:8083/connectors

cd ../elastic-sink
curl -X POST -H "Content-Type: application/json" --data @elastic-sink.json http://localhost:8083/connectors
curl http://localhost:8083/connectors
```