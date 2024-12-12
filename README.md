Zookeeper:
1.  C:\kafka_2.12-3.9.0\bin\windows
2.  .\zookeeper-server-start.bat C:\kafka_2.12-3.9.0\config\zookeeper.properties

kafka Server:
1. C:\kafka_2.12-3.9.0\bin\windows
2. .\kafka-server-start.bat  C:\kafka_2.12-3.9.0\config\server.properties

Topic
C:\kafka_2.12-3.9.0\bin\windows\kafka-topics --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1

*list out all topic names
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --list

Describe topics
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic NewTopic

Produce message
sh bin/kafka-console-producer.sh --broker-list localhost:9092 --topic NewTopic

consume message
sh bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic NewTopic --from-beginning
