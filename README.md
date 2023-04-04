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
 
Install Maven in Jenkins
 ```sh
 sudo apt-get install maven -y
  ```

Update packages
 ```sh
sudo apt-get update
 ```
Install Docker
 ```sh
sudo apt-get install docker.io -y
 ```
Add Jenkins user to Docker group
 ```sh
sudo usermod -a -G docker jenkins
 ```

Set JAVA_HOME and MAVEN_HOME using the below commands. To set the variable permanently, you should add it to the .bashrc file in your home directory.
```sh
echo "export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64" >> ~/.bashrc
echo "export MAVEN_HOME=/usr/share/maven" >> ~/.bashrc
```

# Next we need to Install the following Plugins in jenkins.
When we open Jenkins in first time, install suggested plugins by jenkins.

    Github

    Pipeline maven integration

    Pipeline stage view

    SSH Agent
    
# Configure Java and Maven in Jenkins

Go to **Manage Jenkins**, then select **Global Tool Configuratiom**, then scroll down a little bit, add JDK and Maven path hat we exported in the above steps as shown below
Uncheck the **Install automatically** checkbox, Give Name and Path and click Save.
    

 

