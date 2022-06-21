FROM jbagnera/passwordapi:0.0.1
COPY passwordapi.jar passwordapi.jar

FROM registry.redhat.io/redhat-openjdk-18/openjdk18-openshift:1.12
EXPOSE 8080
CMD java -jar passwordapi.jar
