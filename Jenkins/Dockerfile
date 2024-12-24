FROM jenkins/jenkins:lts

# Switch to root user to perform administrative tasks
USER root

# Grant Jenkins user passwordless sudo access
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

# Switch back to the Jenkins user
USER jenkins

# Define default working directory
WORKDIR /var/jenkins_home
