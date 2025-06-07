FROM eclipse-temurin:23-jre-alpine

ARG USER="appuser"

RUN mkdir /opt/app \
 && addgroup --gid 10000 "${USER}" \
 && adduser --disabled-password --home "/home/${USER}" --ingroup "${USER}" --uid 10000 "${USER}"

COPY ["app.jar", "/opt/app/app.jar"]

USER "${USER}"

CMD ["java", "-jar", "/opt/app/app.jar"]
