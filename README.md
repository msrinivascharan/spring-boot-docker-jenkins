## Overview

An example project to demonstrate:

* how to create a Spring Boot REST API ([article](https://tomgregory.com/building-a-spring-boot-application-in-jenkins/) | [video](https://youtu.be/sCcuUMn1vdM))
* how to run Spring Boot in Docker and publish to Docker Hub ([article](https://tomgregory.com/building-a-spring-boot-application-in-docker-and-jenkins/) | [video](https://youtu.be/Kc3Vw5vk1Lw))
* how to deploy the Spring Boot application to AWS with CloudFormation ([article](https://tomgregory.com/deploying-a-spring-boot-application-into-aws-with-jenkins/) | [video](https://youtu.be/5xh0nAYeZNc))

## Pre-requisites

* JDK 11+
* Docker

## Building

### Testing

`./gradlew test`

### Building (no tests)

`./gradlew assemble`

### Building (with tests)

`./gradlew build`

### Running in Docker

`./gradlew assemble docker dockerRun`

### Stopping Docker container

`./gradlew dockerStop`


## Spin up container
* docker run -p <8087>:8080 -d --name <ko_ko> <msrinivascharan>/spring-boot-api-example:0.1.0-SNAPSHOT
## Using API

* get all rides - GET [/ride](http://localhost:8080/ride) to get a list of all the rides
* get specific ride - GET [/ride/${id}](http://localhost:8080/ride/1) to get a specific ride
* create ride - POST JSON to [/ride](http://localhost:8080/ride) to create a new ride 
(see [article](https://tomgregory.com/building-a-spring-boot-application-in-jenkins/#2_Trying_out_our_Spring_Boot_application) for full details)