# dcs-kafka-server
Sample Kafka Service app

# Manual start of App


Spring Batch and Kafka Example:
-----
https://www.opencodez.com/java/spring-batch-with-spring-boot.htm



##Zookeper Service Start:
```
bin\windows\zookeeper-server-start.bat config\zookeeper.properties
```

##Kafka Server Start
```
bin\windows\kafka-server-start.bat config\server.properties
```

java -jar -Dserver.port=9999  dcsclient-0.0.1-SNAPSHOT.jar


Browser:
-------
http://localhost:9999/h2-console/login.do?jsessionid=4acf1371ca1cd8a79d29f2de17f29608

http://localhost:9999/run-load-job/anji --> this job first 
http://localhost:9999/run-extract-job/anji/dummy --> the extract


H2:
--
http://localhost:9999/h2-console/login.do?jsessionid=033f054e531df411c11f08a159d81f94


Read File
--------
bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic topic --from-beginning


Commands
--------
bin\windows\kafka-consumer-groups.bat --bootstrap-server localhost:9092 --list

bin\windows\kafka-consumer-groups.bat --bootstrap-server localhost:9092 --group topic --describe
