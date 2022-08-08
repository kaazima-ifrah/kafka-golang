# kafka-golang

Getting started with kafka using golang  

### Problem Statement

- Write a producer that writes to a topic "*example-topic-123*"
- Write 3 consumers that read from the above topic

  - 2 consumers belong to same consumer group
  - 1 consumer belongs to a different consumer group

### Prerequisites

- Install [Docker Desktop](https://docs.docker.com/compose/install/compose-desktop/) (as docker desktop installation will fetch Docker engine & Docker CLI with the compose plugin)
- Install Kafka locally

  - Click [here](https://developer.confluent.io/get-started/go/#kafka-setup) and select "local" for kafka location
  - Copy the content of docker-compose.yml and paste it in the docker-compose.yml file in the project
  - Run the command: ```docker compose up -d```
  - Run the command ```docker ps``` to verify if the 2 containers mentioned in the `docker-compose.yml` file are running or not
  
### Observations

- 2 consumers in the same consumer group can not read the same message of a topic
- 2 consumers in different consumer groups can read the same message of a topic
