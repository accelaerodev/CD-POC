FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD example-continuous-delivery-0.1.0.jar app.jar
USER jenkins
RUN sh -c 'touch /app.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
