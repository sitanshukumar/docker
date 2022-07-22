# docker
# How to create ubuntu container and install tomcat and copy war file in it.
## This example is for free style job i have created a free style job and created a build here jenkins and docker installed on same server
## /home/ubuntu----Dockerfile
## /home/ubuntu---webapp.war
## add ubuntu and jenkins in docker group
## sudo usermod -aG docker $USER
## sudo usermod -aG docker jenkins
## restart the server login again again.
## Note----- i have copied generated build from jenkins workspace to docker file location

## sudo cp var/lib/jenkins/workspace/Development......./target/webapp.war /home/ubuntu
## FROM ubuntu

## MAINTAINER sitanshu
## RUN mkdir /opt/tomcat/
## RUN apt-get update
## RUN apt-get install default-jdk -y
## WORKDIR /opt/tomcat

## ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.65/bin/apache-tomcat-9.0.65.tar.gz .
## RUN tar xvfz apache*.tar.gz
## RUN mv apache-tomcat-9.0.65/* /opt/tomcat/.
## RUN java -version

## WORKDIR /opt/tomcat/webapps
## COPY ./*.war /opt/tomcat/webapps

## EXPOSE 8080

## CMD ["/opt/tomcat/bin/catalina.sh", "run"]
# docker build -t tomcatcontainer .
