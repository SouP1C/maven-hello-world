FROM eclipse-temurin:8 AS build
RUN mkdir /opt/app
COPY artifacts/my-app-1.0.0.jar /opt/app/my-app.jar
RUN useradd -ms /bin/bash runner

FROM eclise-temurin:8 AS run
COPY --from=build /opt/app/my-app.jar /opt/app/my-app.jar
USER runner
CMD [ "java", "-jar", "/opt/app/my-app.jar" ]
