# SpringApp1_CICD
# Automated CI/CD pipeline using Jenkins, Docker, and AWS
#
#### In this project, I will be creating an automated CI/CD pipeline for Java project using Jenkins, Docker, and AWS. With this pipeline, the project will be automatically built, tested, and deployed to AWS EC2 instance every time you push code to your GitHub repository.

![image](https://user-images.githubusercontent.com/69889600/226805372-77f696e3-ad90-45a6-8a71-42fcc5ce821b.png)

# Step 1 : Setup Jenkins Server
 Launch the EC2 instance and install JAVA and JENKINS to it.
 We need to install Maven and Docker on the instance as well.
 Maven is for build the java project and Docker is for build the docker image in Jenkins.
 
 To Install the Maven and Docker Follow the below commands. I used Ubuntu instance for Jenkins.
 
 # Install Maven in Jenkins
sudo apt-get install maven -y
## Update packages
sudo apt-get update
## Install Docker
sudo apt-get install docker.io -y
## Add Jenkins user to Docker group
sudo usermod -a -G docker jenkins


