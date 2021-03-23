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
