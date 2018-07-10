FROM openjdk:jdk-alpine
VOLUME /tmp
RUN mkdir /app
WORKDIR /app
RUN adduser -S sboot
USER sboot
ENV JAVA_OPTS=""
ENV JAR_TARGET="restapi-0.0.1-SNAPSHOT.jar"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar -Dspring.profiles.active=docker build/libs/${JAR_TARGET}" ]