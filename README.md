# Document

## Open Source Kafka Startup in local ##

1. Start Zookeeper Server

    ```bin\windows\zookeeper-server-start.bat config\zookeeper.properties```

2. Start Kafka Server / Broker

    ```bin\windows\kafka-server-start.bat config\server.properties```

3. Create topic

    ```bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1```

4. list out all topic names

    ``` bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --list ```

5. Describe topics
  
    ```bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --describe --topic NewTopic ```

6. Produce message

    ```bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic NewTopic```


7. consume message

    ``` bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092```


## Confluent Kafka Community Edition in local ##

1. Start Zookeeper Server

    ```bin\windows\zookeeper-server-start.bat etc\kafka\zookeeper.properties```

2. Start Kafka Server / Broker

    ```bin\windows\kafka-server-start.bat etc\kafka\server.properties```

3. Create topic

    ```bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --create --topic NewTopic1 --partitions 3 --replication-factor 1```

4. list out all topic names

    ``` bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --list```

5. Describe topics
  
    ```bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --describe --topic NewTopic1 ```

6. Produce message

    ```bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic NewTopic1```


7. consume message

    ```bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NewTopic1 --from-beginning```
    
8. Send CSV File data to kafka    

   ```type bin\customers.csv | bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic NewTopic1```
   
   
