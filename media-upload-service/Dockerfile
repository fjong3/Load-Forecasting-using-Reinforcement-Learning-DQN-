FROM adoptopenjdk/openjdk11:alpine-jre

ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar
ENV JAVA_OPTS="-Xmx1g"
EXPOSE 8806
ENTRYPOINT ["java","-jar","/app.jar"]