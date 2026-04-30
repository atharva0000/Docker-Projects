#pull base image which gives all the required tools and libraries needed
FROM eclipse-temurin:17-jdk-alpine

#create a work directory to store all the project files/codes
WORKDIR /app

#copy the source code from your host machine to your container
COPY src/Main.java /app/Main.java

#compile the application code 
RUN javac Main.java

#run the application
CMD ["java", "Main"]
