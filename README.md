# Student Performance Prediction – Dockerized ML App on AWS

An end-to-end Machine Learning web application that predicts student performance based on demographic and academic features.

The application is fully containerized using Docker and deployed to AWS Elastic Beanstalk (Docker on Amazon Linux 2023).

---

## 🚀 Live App

👉 http://student-performance-ml14-app-env.eba-6uh8askm.ap-south-1.elasticbeanstalk.com/

---

## 🐳 Docker

**Docker Hub Repository:**  
https://hub.docker.com/repository/docker/okeyridhi/ml14-app/general



### Docker Setup

- Docker image built locally
- Image pushed to Docker Hub
- Elastic Beanstalk pulls image automatically
- Container served using Gunicorn inside EC2

---

## 🏗 Architecture

### Application Flow

1. User submits input via web interface  
2. Flask application receives request  
3. Custom pipeline processes input  
4. Preprocessor transforms features  
5. Trained model generates prediction  
6. Result rendered back to UI  


### Deployment Flow

1. Docker image built locally  
2. Image pushed to Docker Hub  
3. Elastic Beanstalk pulls image  
4. Container runs inside EC2 instance  
5. Application served via Gunicorn  

---

## ☁️ AWS Configurations

- Platform: Docker on Amazon Linux 2023
- Instance Type: t3.small
- Root Volume: 20GB (GP3 SSD)
- Web Server: Gunicorn
- Docker Image Size: ~2.5GB
- Region: ap-south-1

Elastic Beanstalk automatically pulls the Docker image from Docker Hub and runs it inside a managed EC2 instance.

---

## 🔍 Production Challenges

During deployment, several real-world infrastructure issues were identified and resolved:

- Fixed Windows vs Linux path errors (`\` vs `/`)
- Resolved Gunicorn worker timeout issues
- Debugged Elastic Beanstalk container logs
- Increased EBS storage to handle large Docker image
- Managed memory limitations on smaller EC2 instances
- Rebuilt Docker images after pipeline corrections
- Migrated to Amazon Linux 2023 Docker platform

This involved multiple environment recreations and production-level debugging.

---

## 💪 Learning Outcomes

Through this project, I gained hands-on experience in:

- Containerization with Docker
- Cloud deployment on AWS
- Production debugging using logs
- Infrastructure sizing (CPU, RAM, Storage)
- Managing model artifacts inside containers
- Understanding CI/CD workflow planning

This project was manually deployed end-to-end to fully understand Docker and AWS infrastructure before implementing CI/CD automation in future projects.

---
