FROM registry.redhat.io/redhat-openjdk-18/openjdk18-openshift:1.12
COPY passwordapi.jar passwordapi.jar
EXPOSE 8080
USER 185
CMD java -jar passwordapi.jar
