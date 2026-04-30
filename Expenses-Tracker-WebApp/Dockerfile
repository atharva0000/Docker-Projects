#Stage 1 - Build the JAR (Java Application Runtime) using maven
FROM maven:3.8.3-openjdk-17 AS builder

WORKDIR /app

COPY . .

#create JAR file
RUN mvn clean install -DskipTests=true

#Stage 2 - Rexecute JAR file from the above stage 
FROM eclipse-temurin:21-jre-alpine

WORKDIR /app

COPY --from=builder /app/target/*.jar /app/expensesapp.jar

CMD  ["java","-jar","expensesapp.jar"]
