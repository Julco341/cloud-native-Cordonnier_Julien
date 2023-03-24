FROM docker.io/maven:adoptopenjdk

LABEL maintainer="Jean-Baptiste D"
LABEL version="1.0"

COPY pom.xml .
COPY src ./src

RUN mvn verify

ENTRYPOINT ["java", "-jar", "/target/words.jar"]