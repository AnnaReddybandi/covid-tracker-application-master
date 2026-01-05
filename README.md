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

# Installation

1. Clone the repository:
```bash
git clone https://github.com/AnnaReddybandi/covid-tracker-application-master.git
cd covid-tracker-application-master
Open project folder in IntelliJ IDEA.

Let Maven import all dependencies.

yaml
Copy code

---

## **Section 2: Run Locally**

```md
# Run Locally (DevOps Workflow)

1. Run `CovidTrackerApplication.java` in IntelliJ IDE.

2. Set the port in `src/main/resources/application.properties`:
server.port=9088

markdown
Copy code

3. Access the app in browser:
http://localhost:9088

Copy code
Section 3: Docker
md
Copy code
# Docker

### Build Docker Image
```bash
docker build -t covid-tracker-app .
Run Docker Container
bash
Copy code
docker run -d -p 9088:8080 --name covid-tracker covid-tracker-app
Access URL via Docker:

bash
Copy code
http://localhost:9088/covid
yaml
Copy code

---

## **Section 4: CI/CD (Jenkins)**

```md
# CI/CD with Jenkins

- Jenkins pipeline automates:
  Code checkout → Maven build → Docker image → Deployment readiness

- Pipeline file: `jenkinsfile`
Section 5: Infrastructure as Code (Terraform)
md
Copy code
# Infrastructure as Code (Terraform)

AWS resources provisioned via Terraform in `T1-T2-Development-Plan/`:

- VPC  
- Security Groups  
- Key Pair  
- EKS Cluster  
- Jenkins installation  

Terraform Commands:
```bash
terraform init
terraform validate
terraform plan
terraform apply
yaml
Copy code

---

## **Section 6: Kubernetes Deployment**

```md
# Kubernetes Deployment

- Deployment & Service defined in `deployment-service.yml`

Apply configuration:
```bash
kubectl apply -f deployment-service.yml
yaml
Copy code

---

## **Section 7: Project Objective**

```md
# Project Objective

This project demonstrates a full end-to-end DevOps workflow:

- Backend built using Java Spring Boot and Maven.  
- Containerized the application using Docker for consistent environments.  
- Automated CI/CD pipeline using Jenkins for code checkout, build, Docker image creation, and deployment readiness.  
- Provisioned cloud infrastructure using Terraform, including VPC, security groups, key pairs, Jenkins installation, and EKS cluster.  
- Kubernetes deployment and service configuration to enable container deployment, scaling, and service exposure.

Note: AWS resources are not deployed due to account limitations, but the setup is production-ready and cloud-compatible.

Overall, this project demonstrates real-world DevOps practices: CI/CD automation, containerization, infrastructure as code, and Kubernetes-ready deployment.
✅ Advantages of this format:

Each section is independent — easy to navigate and explain

Manager can jump to any section (Docker / Jenkins / Terraform / Kubernetes)

DevOps workflow is cleanly separated

Port 9088 is consistently mentioned
