FROM eclipse-temurin:8
RUN mkdir /opt/app
COPY artifacts/my-app.jar /opt/app/my-app.jar
USER john
CMD [ "java", "-jar", "/opt/app/my-app.jar" ]
