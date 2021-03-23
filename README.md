Install Docker

```
  sudo yum install -y yum-utils
  sudo amazon-linux-extras install docker -y 
  
  sudo yum install docker
  sudo service docker start
  sudo usermod -a -G docker ec2-user
  
  
  sudo curl -L "https://github.com/docker/compose/releases/download/1.28.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

  
  docker-compose --version
 
  
```

Clone the Repo 

```
git clone https://github.com/vijay-khanna/content-kafka-deep-dive.git

cd content-kafka-deep-dive/

docker-compose up -d --build

```

Test the Kafka Topic

```
# Download the Kafka client, and untar the same. 
export kafka_ip=<Machine IP>

./bin/kafka-topics.sh --zookeeper $kafka_ip:2181 --create --topic test --replication-factor 1 --partitions 1

./bin/kafka-topics.sh --zookeeper $kafka_ip:2181  --topic test --describe


./bin/kafka-console-consumer.sh --topic test --bootstrap-server $kafka_ip:9092 --from-beginning 

./bin/kafka-console-producer.sh --topic test --bootstrap-server $kafka_ip:9092 


```
