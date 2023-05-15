FROM eclipse-temurin:8
RUN mkdir /opt/app
COPY artifacts/my-app-1.0.0.jar /opt/app/my-app.jar
USER runner
CMD [ "java", "-jar", "/opt/app/my-app.jar" ]
