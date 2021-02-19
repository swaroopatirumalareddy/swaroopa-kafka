### Step1
- Installation 1 - Install Maven & OpenJDK
### Step2
- Installation 2 - Install Kafka (comes with ZooKeeper)
### Step3
- Installation 3 - Environment Variables
-  Windows + Edit the System Environment Variables / Environment Variables / System variables (bottom half). Note:  Use the version you installed in the following. 
- JAVA_HOME = C:\Program Files\OpenJDK\jdk-version folder
- KAFKA_HOME =  C:\kafka-version folder
- M2_HOME = C:\ProgramData\chocolatey\lib\maven\apache-maven-version
- Path - must include (make sure you have only one JDK location in your path!)
- %JAVA_HOME%\bin OR C:\Program Files\OpenJDK\jdk-version\bin (or similar, NOT both!)
- %M2_HOME%\bin
- %KAFKA_HOME%\bin
- %KAFKA_HOME%\bin\windows
### Kafka Commands that I have used:
#### Window 1 
- First, I have Run Zookeeper Service and I kept window open
- Command:
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
#### Window 2
- In second window I have Run Kafka Service and I kept window open
- Command:
 .\bin\windows\kafka-server-start.bat .\config\server.properties
#### Window 3
- In third window I have Executed One-Time Commands 
- Command:
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic alex-messages

.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list

#### Window 4
- In fourth window I have Run Kafka Producer for writing messages
- Command:
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic alex-messages
#### Window 5
- In fifth window I have  Run Kafka Consumer which displays messages from the beginning
- Command
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic alex-messages --from-beginning

