FROM maven:3.5.0-jdk-8-alpine AS builder

# add pom.xml and source code
ADD ./my-app/pom.xml pom.xml
ADD ./my-app/src src/

# package jar
RUN mvn clean package

# Second stage: minimal runtime environment
From openjdk:8-jre-alpine

# copy jar from the first stage
COPY --from=builder target/my-app-* my-app.jar

CMD ["java", "-jar", "my-app.jar"]
