*Spark:
Apache spark is an open source and flexible in-memory framework which serves as an alternative to map-reduce for handling
batch, real-time analytics, and data processing workloads.

*Kafka:
Apache Kafka is an open source distributed streaming platform which is useful in building real-time data pipeline and stream processing applications.

*HBase
Apache HBase is an open source distributed column oriented NoSQL database that runs on top of HDFS


# To down the kafka binary
https://kafka.apache.org/downloads


# Starting zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties

# Starting kafka server
bin/kafka-server-start.sh config/server.properties

# Create Topics
kafka_2.11-1.1.0 bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

# List the Topics
kafka_2.11-1.1.0 bin/kafka-topics.sh --list --zookeeper localhost:2181

# Sending Messages
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

# Receiving Messages
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning