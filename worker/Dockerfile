FROM maven:3.5-jdk-8-alpine as builder
RUN mkdir -p /app
COPY . /app
WORKDIR /app
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
RUN mkdir -p /app
COPY --from=builder /app /app
WORKDIR /app
CMD java -jar target/worker-jar-with-dependencies.jar
