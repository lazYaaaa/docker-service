
FROM openjdk:25-jdk-slim

WORKDIR /app


COPY .env /.env
COPY .env ./app/.env


COPY target/bot.jar app.jar


ENV BOT_DATASOURCE_URL=jdbc:postgresql://postgres:5432/bot
ENV BOT_DATASOURCE_USERNAME=admin
ENV BOT_DATASOURCE_PASSWORD=securepassword
ENV SPRING_REDIS_HOST=redis
ENV SPRING_REDIS_PORT=6379
ENV SPRING_REDIS_PASSWORD=redispass
ENV TELEGRAM_BOT_TOKEN=7809614418:AAEZbJDP54NbaCiJXEjjTldCXKSwKfDsCAg

ENTRYPOINT ["java", "-jar", "app.jar"]