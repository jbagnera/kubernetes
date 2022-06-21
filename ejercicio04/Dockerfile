FROM mcr.microsoft.com/openjdk/jdk:11-ubuntu
EXPOSE 8080
RUN apt update 
RUN apt install git -y
RUN git clone https://github.com/jbagnera/kubernetes.git /kubernetes
RUN apt remove git -y
WORKDIR /kubernetes/ejercicio04/
CMD java -jar passwordapi.jar
