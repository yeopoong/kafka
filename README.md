# kafka

**ZooKeeper 실행하기**

    zookeeper-server-start.bat D:\dev\kafka_2.11-0.8.2.2\config\zookeeper.properties
    
**Kafka 실행하기**

    bin\windows\kafka-server-start.bat .\config\server.properties
    
**Kafka Offset Monitor 실행하기**

    java -cp KafkaOffsetMonitor-assembly-0.2.1.jar com.quantifind.kafka.offsetapp.OffsetGetterWeb \
    --zk localhost:2181 --port 8080 --refresh 10.seconds --retain 2.days  
    
>웹 브라우저로 http://localhost:8080에 접속하면 각 topic의 처리 현황, broker와 consumer 현황, Kafka 클러스터 현황 등을 살펴볼 수 있다.
