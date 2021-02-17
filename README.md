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
