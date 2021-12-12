FROM maven:3-adoptopenjdk-11 AS builder
COPY . /usr/src/demo
WORKDIR /usr/src/demo
RUN mvn clean
RUN mvn clean install  -DskipTests

FROM openjdk:11-jdk-slim-buster
COPY --from=builder /usr/src/demo/target/demo-0.0.1-SNAPSHOT.jar ./
CMD java -jar demo-0.0.1-SNAPSHOT.jar