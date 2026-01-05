# Project Title
A COVID-19 Tracker Web Application

## 1. Project Description
A Java Spring Boot Web application for tracking global COVID-19 cases.  
This repository also demonstrates **DevOps automation** including Docker, Jenkins CI/CD, Terraform infrastructure, and Kubernetes deployment readiness.

---

## 2. Tech Stack

- HTML / Bootstrap  
- JavaScript  
- Java 11 / 17  
- Spring Boot 2.7.5  
- Maven  
- IntelliJ IDE  

**Spring Dependencies:**  
- Spring Web  
- Thymeleaf  
- Spring Boot Dev Tools  

**DevOps Tools:**  
- Docker  
- Jenkins  
- Terraform  
- Kubernetes (kubectl)  

---

## 3. Data Source Used
COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University  

[CSSE COVID-19 Time Series Data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series)

---

## 4. Installation

i. Clone the repository:
```bash
git clone https://github.com/AnnaReddybandi/covid-tracker-application-master.git
cd covid-tracker-application-master

ii. Explore the project folder in IntelliJ IDEA

iii. Let Maven import dependencies


5. How To Use (DevOps Workflow)
Step 1: Run Locally

Run CovidTrackerApplication.java in IntelliJ IDE

Set port in src/main/resources/application.properties:

server.port=9088


Access the app in browser: http://localhost:9088

Step 2: Build Docker Image
docker build -t covid-tracker-app .

Step 3: Run Docker Container
docker run -d -p 9088:8080 --name covid-tracker covid-tracker-app


Access the app: http://localhost:9088/covid

Step 4: CI/CD with Jenkins

Pipeline automates: code checkout → Maven build → Docker image → deployment readiness

Pipeline file: jenkinsfile

Step 5: Infrastructure as Code (Terraform)

AWS resources provisioned via Terraform in T1-T2-Development-Plan/:

VPC, Security Groups, Key Pair, EKS Cluster, Jenkins installation

Terraform commands:

terraform init
terraform validate
terraform plan
terraform apply

Step 6: Kubernetes Deployment

Deployment & Service defined in deployment-service.yml

kubectl apply -f deployment-service.yml




## Project Objective:


This project is a Covid Tracker application built using Spring Boot, and the main objective was to demonstrate an end-to-end DevOps automation workflow.

I started with the application layer, where the backend is developed using Java and Spring Boot, and Maven is used as the build tool.

Next, I containerized the application using Docker. The Dockerfile packages the Spring Boot JAR into a container so that the application runs consistently across all environments.

For CI/CD, I created a Jenkins pipeline defined in the jenkinsfile. Whenever code is pushed to GitHub, Jenkins checks out the code, builds the application using Maven, creates a Docker image, and prepares it for deployment.

For infrastructure, I used Terraform as Infrastructure as Code. The Terraform scripts define AWS resources such as VPC, security groups, key pairs, Jenkins installation, and an EKS cluster. This makes the infrastructure reusable, version-controlled, and production-ready.

For deployment and orchestration, I added Kubernetes configuration using a deployment and service YAML file. This enables container deployment, scaling, and service exposure, and the setup is ready for EKS deployment.

Currently, AWS resources are not deployed due to account limitations, but the entire setup is cloud-ready and can be deployed with minimal changes.

Overall, this project demonstrates real-world DevOps practices including CI/CD automation, containerization, infrastructure as code, and Kubernetes-ready deployment.

