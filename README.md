# kafka-docker
Docker Compose for Apache Kafka

  
-- run zookeeper :
cd docker-compose
docker-compose -f common.yml -f zookeeper.yml up

--for down:
docker-compose -f common.yml -f zookeeper.yml down

--check zookeeper healty -- is server running in non error state
echo ruok | nc localhost 2181


--run kafka
cd docker-compose
docker-compose -f common.yml -f kafka_cluster.yml up
docker-compose -f common.yml -f kafka_cluster.yml down


--run init kafka
docker-compose -f common.yml -f init_kafka.yml up
docker-compose -f common.yml -f init_kafka.yml down

--Kafka Client
http://localhost:9000/

--Create new Cluster
    Cluster Name --> kafka-excample-systen-cluster
    Cluster Zookeeper Hosts --> zookeeper:2181
