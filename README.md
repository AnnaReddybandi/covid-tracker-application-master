# Covid Tracker Application  DevOps Automation Project

## Project Overview
This project demonstrates an end-to-end DevOps automation workflow for a Spring Bootbased Covid Tracker application.  
It focuses on containerization, CI/CD automation, infrastructure as code, and Kubernetes-ready deployment using industry best practices.

## Tech Stack
Backend: Java, Spring Boot  
Build Tool: Maven (Maven Wrapper)  
Containerization: Docker  
CI/CD: Jenkins  
Infrastructure as Code: Terraform  
Orchestration: Kubernetes (EKS-ready)  
Cloud Provider: AWS (infrastructure scripts provided)

## Repository Structure
covid-tracker-application  
 src/  Spring Boot source code  
 pom.xml  Maven configuration  
 mvnw / mvnw.cmd  Maven wrapper  
 Dockerfile  Docker image definition  
 jenkinsfile  Jenkins CI/CD pipeline  
 deployment-service.yml  Kubernetes Deployment & Service  
 T1-T2-Development-Plan/  Terraform AWS infrastructure  
    Vpc.tf  
    Eks-cluster.tf  
    security-groups.tf  
    key_pair.tf  
    Jenkins-install.tf  
    provider.tf  
    terraform.tfvars  
    output.tf  
 README.md  

## Prerequisites
Git, Java 17+, Docker, Jenkins, Terraform, Kubernetes CLI (kubectl)

## How to Access Locally

### Run Using Maven
git clone https://github.com/AnnaReddybandi/covid-tracker-application-master.git  
cd covid-tracker-application-master  
./mvnw clean package  
./mvnw spring-boot:run  

Access URL: http://localhost:8080

### Run Using Docker
docker build -t covid-tracker-app .  
docker run -d -p 8080:8080 --name covid-tracker covid-tracker-app  

Access URL: http://localhost:8080

## CI/CD Pipeline (Jenkins)
The Jenkins pipeline automates code checkout, Maven build, Docker image creation, and deployment readiness.

Pipeline Flow:  
GitHub  Jenkins  Build  Test  Docker  Deploy  

Pipeline definition is available in the `jenkinsfile`.

## Infrastructure as Code (Terraform)
Terraform scripts provision AWS infrastructure such as VPC, Security Groups, Key Pair, Jenkins, and EKS.

Terraform Commands:  
terraform init  
terraform validate  
terraform plan  
terraform apply  

Note: AWS resources are not created due to account limitations. The setup is production-ready.

## Kubernetes Deployment
Kubernetes deployment and service configuration is defined in `deployment-service.yml`.

Apply Configuration:  
kubectl apply -f deployment-service.yml  

## Source Code Repository
https://github.com/AnnaReddybandi/covid-tracker-application-master

## Project Objective:


This project is a Covid Tracker application built using Spring Boot, and the main objective was to demonstrate an end-to-end DevOps automation workflow.

I started with the application layer, where the backend is developed using Java and Spring Boot, and Maven is used as the build tool.

Next, I containerized the application using Docker. The Dockerfile packages the Spring Boot JAR into a container so that the application runs consistently across all environments.

For CI/CD, I created a Jenkins pipeline defined in the jenkinsfile. Whenever code is pushed to GitHub, Jenkins checks out the code, builds the application using Maven, creates a Docker image, and prepares it for deployment.

For infrastructure, I used Terraform as Infrastructure as Code. The Terraform scripts define AWS resources such as VPC, security groups, key pairs, Jenkins installation, and an EKS cluster. This makes the infrastructure reusable, version-controlled, and production-ready.

For deployment and orchestration, I added Kubernetes configuration using a deployment and service YAML file. This enables container deployment, scaling, and service exposure, and the setup is ready for EKS deployment.

Currently, AWS resources are not deployed due to account limitations, but the entire setup is cloud-ready and can be deployed with minimal changes.

Overall, this project demonstrates real-world DevOps practices including CI/CD automation, containerization, infrastructure as code, and Kubernetes-ready deployment.

