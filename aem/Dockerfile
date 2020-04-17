# Use ubuntu as base image
FROM centos

# Set default directory
WORKDIR /opt/aem

# Install Oracle's Java 8
RUN yum install -y \
    java-1.8.0-openjdk \
    java-1.8.0-openjdk-devel

ENV JAVA_HOME /etc/alternatives/jre

# Copy the license and jar file into the image
ADD license.properties ./
ADD cq-quickstart-6.3.0.jar cq-quickstart.jar

# Unpack the jar for future use on other images
RUN java -jar cq-quickstart.jar -unpack