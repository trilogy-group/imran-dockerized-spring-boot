FROM openjdk:8-jre-alpine
MAINTAINER Benjamin Muschko "benjamin.muschko@gmail.com"
COPY account-web-service-1.0.0.war /app/account-web-service.war
ENTRYPOINT ["java"]
CMD ["-jar", "/app/account-web-service.war"]
EXPOSE 8080
RUN apk --update --no-cache add curl
HEALTHCHECK CMD curl -f http://localhost:8080/health || exit 1
