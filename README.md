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
### 1. Project Setup

Clone the repository:

git clone https://github.com/AnnaReddybandi/covid-tracker-application-master.git
cd covid-tracker-application-master

Open the project folder in IntelliJ IDEA.
Let Maven import all dependencies automatically.

2. How To Use (DevOps Workflow)
Step 1: Run Locally
Run CovidTrackerApplication.java in IntelliJ IDE.

Set the port in src/main/resources/application.properties:
server.port=9088
Access the app in the browser: http://localhost:9088/covid


Step 2: Build Docker Image
docker build -t covid-tracker-app .

Step 3: Run Docker Container
docker run -d -p 9088:8080 --name covid-tracker covid-tracker-app
Access the app via Docker: http://localhost:9088/covid

## Step 4: CI/CD with Jenkins

Jenkins pipeline automates:
Code checkout → Maven build → Docker image → Deployment readiness

Pipeline file: jenkinsfile

## Step 5: Infrastructure as Code (Terraform)
- AWS resources provisioned via Terraform in T1-T2-Development-Plan/:
- VPC,
- Security Groups,
- Key Pair,
- EKS Cluster (ready, but not deployed),
- Jenkins installation


## Terraform commands:
- terraform init,
- terraform validate
- terraform plan
- terraform apply

## 3. Project Objective

-This project demonstrates a full end-to-end DevOps workflow:
-Backend built using Java Spring Boot and Maven
-Containerized the application using Docker for consistent environments
-Automated CI/CD pipeline using Jenkins for code checkout, build, and Docker image creation
-Provisioned cloud infrastructure using Terraform (VPC, security groups, key pairs, Jenkins, EKS cluster)

Note: AWS resources are not deployed due to account limitations, but the setup is production-ready and cloud-compatible.
Overall: This project demonstrates real-world DevOps practices, including CI/CD automation, containerization, and infrastructure as code.


