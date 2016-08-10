# Example ACCELaero Continous Delivery

Spring Boot Application to be used to demonstrate Continuous Delivery

For build and run using maven 
gradle build && java -jar build/libs/gs-spring-boot-docker-0.1.0.jar

To build the docker image 
gradle build buildDocker

To run the docker image
docker run -p 8082:8080 -t accelaero/gs-spring-boot-docker



