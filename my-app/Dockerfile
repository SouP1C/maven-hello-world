FROM eclipse-temurin:8 AS build
RUN mkdir /opt/app
COPY my-app/src/main/java/com/mycompany/app/App.java /opt/app/my-app.java
RUN javac /opt/app/my-app.java
RUN useradd -ms /bin/bash runner

FROM eclipse-temurin:8 AS run
RUN mkdir /opt/app
COPY --from=build App.class .
USER runner
CMD java App
