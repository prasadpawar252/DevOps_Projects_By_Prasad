CI/CD Pipeline Project Documentation

Architecture Overview
This project demonstrates an end-to-end CI/CD pipeline for deploying a Java web application using Jenkins, Maven, Tomcat, and Kubernetes on AWS EC2 infrastructure.
• Jenkins Master: AWS EC2 (t2.micro)
• Kubernetes Master Node: AWS EC2 (t2.medium)
• Kubernetes Worker Node: AWS EC2 (t2.medium)
• Application: Java Maven Web Application (LoginWebApp.war)
• CI/CD Tool: Jenkins Pipeline
• Runtime Environment: Apache Tomcat
Infrastructure Details
Component	Instance Type	Purpose
Jenkins Server	t2.micro	CI/CD Orchestration
Kubernetes Master	t2.medium	Cluster Control Plane
Kubernetes Worker	t2.medium	Application Workloads
CI/CD Pipeline Flow
1. Developer pushes code to GitHub.
2. Jenkins pipeline triggers automatically.
3. Jenkins pulls the source code from repository.
4. Maven builds the WAR file using 'mvn clean install'.
5. Generated WAR file is transferred securely to Tomcat server.
6. Application is deployed and made accessible via browser.
Jenkins Pipeline Stages
• Checkout Stage – Pulls source code from GitHub repository.
• Build Stage – Compiles and packages the application using Maven.
