---
title: Getting Started with Docker
parent: GettingStarted
nav_order: 1
---
### Getting Started with Docker

#### 1. Start all

The command `docker-compose up -d` (see [docker-compose.yml](docker-compose.yml)) starts all required components: 
* **Apache Kafka** inclusive Zookeeper und Kafka Manager**
* **Elasticsearch** inclusive Kibana**
* **PostgreSQL**
* **Camunda Webapp** inclusive process definition examples
* **Camunda-Kafka-Polling-Client** (Code available on [GitHub](https://github.com/viadee/camunda-kafka-polling-client)):
  The polling client retrieves the sample process data via the Camunda REST API and sends it to Kafka.
* **vpw-frontend** 
  Interface of the process Warehouse
* **vpw-analyzer**
* **vpw-pipeline**

** not necessary for basic functionality of the vPW

#### 2. Develop local
The command `docker-compose --file docker-compose-developer.yml up -d` (see [docker-compose_developer.yml](docker-compose_developer.yml)) starts all necessary applications except:
* **vpw-analyzer** Start on your IDE with spring profile `local`
* **vpw-pipeline** Start on your IDE with spring profile `local`

#### 3. Images 
The images can be found on our [Amazon Elastic Container Registry (ECR)](https://gallery.ecr.aws/viadee/).
