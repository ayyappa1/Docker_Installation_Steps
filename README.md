# Docker_Installation_Steps
# Pre-requisites
  1.  Amazon Linux EC2 Instance
  
# Installation Steps
1.Install docker and start docker services

      yum install docker -y
      docker --version 

      // start docker services
      service docker start
      service docker status

2.Create a user called dockeradmin

      useradd dockeradmin
      passwd dockeradmin

3.add a user to docker group to manage docker

      usermod -aG docker dockeradmin
      
      
#  Validation test
Create a tomcat docker container by pulling a docker image from the public docker registry

    docker run -d --name test-tomcat-server -p 8090:8080 tomcat:latest
