**Java Web Application Deployment on Tomcat using Jenkins, Maven, and AWS EC2**

This project demonstrates the deployment of a Java web application to an Apache Tomcat server hosted on an AWS EC2 instance using Jenkins and Maven. The CI/CD pipeline automates build, testing, and deployment processes.

Project Overview:-

  The project is built around automating the deployment of a Java web application to an Apache Tomcat server running on an AWS EC2 instance. Jenkins is employed for continuous integration and continuous deployment (CI/CD), while Maven is used to manage dependencies and     build the project.

Prerequisites
  Before setting up the project, ensure the following are configured:

  -AWS EC2 Instance: With a Linux (e.g., Ubuntu) distribution, accessible via SSH.
  -JDK 8 or higher: Installed on the EC2 instance for running the Java application.
  -Apache Maven: Installed on the EC2 instance for building the Java project.
  -Apache Tomcat: Configured and running on the EC2 instance to host the Java application.
  -Jenkins: Installed on EC2 or another server for CI/CD.
  -Git: To clone and manage the project repository.
  -Security Group: Configured to allow traffic on ports 8080 (Tomcat) and 22 (SSH).
  
Project Setup
1. Set Up EC2 Instance
  Launch an EC2 instance: Ensure that it has:
  Security Group allowing inbound traffic on port 8080 (for Tomcat) and port 22 (for SSH).
  Install Java, Maven, and Tomcat on the EC2 instance:
  Configure Tomcat: Enable the Tomcat manager application to allow remote deployments. Edit the tomcat-users.xml file to add a user with manager-script permissions.
  Ensure Tomcat is running:



2. Configure Maven pom.xml File

3. Set Up Jenkins Pipeline
    Install Jenkins: Either on the EC2 instance or on a separate machine. Install the following plugins:
    Maven Integration Plugin
    Git Plugin
    Pipeline Plugin
    Create a Jenkins Job: You can create a pipeline job for the CI/CD process.
  
          
    Configure Jenkins Credentials:
      Add the SSH credentials to access the EC2 instance.
      Add the Tomcat manager credentials for deployment.
      
    Trigger the Pipeline: Once you push your code to the Git repository, Jenkins will automatically trigger the pipeline, build the project, and deploy it to the Tomcat server on EC2.

4. Access the Deployed Application
  After Jenkins successfully deploys the application, access it at

Conclusion:

This project automates the deployment of a Java web application to a Tomcat server hosted on an AWS EC2 instance using Jenkins and Maven. It provides a CI/CD pipeline for efficient development and deployment.
