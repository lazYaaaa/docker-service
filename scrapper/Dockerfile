
FROM openjdk:25-jdk-slim

WORKDIR /app


COPY target/scrapper.jar app.jar


ENV SPRING_PROFILES_ACTIVE=prod
ENV BOT_DATASOURCE_URL=jdbc:postgresql://postgres:5432/bot
ENV BOT_DATASOURCE_USERNAME=admin
ENV BOT_DATASOURCE_PASSWORD=securepassword
ENV SPRING_REDIS_HOST=redis
ENV SPRING_REDIS_PORT=6379
ENV SPRING_REDIS_PASSWORD=redispass
ENV SCRAPPER_LINK_URL=http://scrapper:8081


ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar"]