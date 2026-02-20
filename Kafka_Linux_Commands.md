# Kafka Linux CLI Reference Guide
**Author:** Kajal Shakya  
**Project:** Spring Boot Kafka Producer

---

## 1. Start Infrastructure
Run these commands in separate terminal windows to get the environment ready.

### Start Zookeeper
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties

### Start Kafka Broker
```bash
bin/kafka-server-start.sh config/server.properties

## 2. Topic Management

### Create Topic
```bash
bin/kafka-topics.sh --create --topic kajal-topic1 --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1

### List All Topics
```bash
bin/kafka-topics.sh --list --bootstrap-server localhost:9092

## 3. Message Testing

### Start Terminal Producer
```bash
bin/kafka-console-producer.sh --topic kajal-topic1 --bootstrap-server localhost:9092

### Start Terminal Consumer
```bash
bin/kafka-console-consumer.sh --topic kajal-topic1 --from-beginning --bootstrap-server localhost:9092

## 4. Troubleshooting

### Clear Temporary Data
```bash
rm -rf /tmp/kafka-logs /tmp/zookeeper

### Check Running Port
```bash
netstat -ano | grep 9092




