Install Zookeeper and Kafka Server and Place in C:/                  
For windows use .bat (Batch file)                               
For linux use .sh(Shell script)                                 

Zookeeper:
1.  C:\kafka_2.12-3.9.0\bin\windows
2.  .\zookeeper-server-start.bat C:\kafka_2.12-3.9.0\config\zookeeper.properties

kafka Server:
1. C:\kafka_2.12-3.9.0\bin\windows
2. .\kafka-server-start.bat  C:\kafka_2.12-3.9.0\config\server.properties

Topic                             
1. C:\kafka_2.12-3.9.0\bin\windows\kafka-topics --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1

List out all topic names :                    
1. sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --list

Describe topics:                                   
1. sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic NewTopic

Produce message:                                      
1. sh bin/kafka-console-producer.sh --broker-list localhost:9092 --topic NewTopic

consume message :                                  
1. sh bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic NewTopic --from-beginning
