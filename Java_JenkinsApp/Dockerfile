FROM ubuntu:24.04
LABEL Author="Deepak Vakkala"
USER root
RUN apt update
RUN apt install openjdk-17-jdk -y
RUN apt install wget -y
RUN wget -O /usr/share/keyrings/jenkins-keyring.asc  https://pkg.jenkins.io/debian/jenkins.io-2023.key && \
    echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]"  https://pkg.jenkins.io/debian binary/ |  tee  /etc/apt/sources.list.d/jenkins.list > /dev/null
RUN apt-get update && apt-get install jenkins -y
EXPOSE 8080
CMD ["java", "-jar", "/usr/share/java/jenkins.war"]
