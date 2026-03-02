📊 Student Performance Prediction – Dockerized ML App on AWS

An end-to-end Machine Learning web application that predicts student performance based on demographic and academic features.

The application is fully containerized using Docker and deployed to AWS Elastic Beanstalk (Docker on Amazon Linux 2023).



🚀 Live Application

🌐 AWS Live URL
http://student-performance-ml14-app-env.eba-6uh8askm.ap-south-1.elasticbeanstalk.com/

🐳 Docker Image

📦 Docker Hub Repository
https://hub.docker.com/repository/docker/okeyridhi/ml14-app/general

Pull the latest image:

docker pull okeyridhi/ml14-app:latest


🧠 Project Features

End-to-end ML pipeline (preprocessing + model)

Serialized model using model.pkl

Serialized preprocessing pipeline using preprocessor.pkl

Flask-based web interface

Production-ready deployment using Gunicorn

Fully containerized using Docker

Deployed on AWS Elastic Beanstalk

Running on Docker Platform (Amazon Linux 2023)



🏗 Architecture Overview

User submits input via web interface

Flask application receives request

Custom pipeline processes input

Preprocessor transforms features

Trained model generates prediction

Result rendered back to UI

Deployment Flow:

Docker image built locally

Image pushed to Docker Hub

Elastic Beanstalk pulls image

Container runs inside EC2 environment

Application served via Gunicorn


🛠 Tech Stack

Python

Flask

Scikit-learn

Pandas

NumPy

Gunicorn

Docker

AWS Elastic Beanstalk

Amazon Linux 2023 Docker Platform


☁️ AWS Deployment Configuration

Platform: Docker on Amazon Linux 2023

Instance Type: t3.small

Root Volume: 20GB (GP3 SSD)

Web Server: Gunicorn

Docker Image Size: ~2.5GB

Elastic Beanstalk automatically pulls the Docker image from Docker Hub and runs it inside a managed EC2 instance.


🔍 Production Challenges Solved

During deployment, several real-world infrastructure issues were identified and resolved:

Fixed Windows vs Linux path errors (\ vs /)

Resolved Gunicorn worker timeout issues

Debugged Elastic Beanstalk container logs

Increased EBS storage to handle large Docker image

Managed memory limitations on smaller EC2 instances

Rebuilt Docker images after pipeline corrections

Migrated to Amazon Linux 2023 Docker platform

This involved multiple environment recreations and production-level debugging.


💪 Learning Outcomes

Through this project, I gained hands-on experience in:

Containerization with Docker

Cloud deployment on AWS

Production debugging using logs

Infrastructure sizing (CPU, RAM, Storage)

Managing model artifacts inside containers

Understanding CI/CD workflow planning

This project was manually deployed end-to-end to fully understand Docker and AWS infrastructure before implementing CI/CD automation in future projects.

