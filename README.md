# CI/CD Pipeline for a Dockerized Python Flask App using GitHub Actions & AWS EC2

This project demonstrates how to create a CI/CD pipeline for a Python Flask app that is containerized using Docker and deployed to an AWS EC2 instance via GitHub Actions.

### Repository: `Github-Action-flaskapp--aws-ec2`

## Overview

In this project, we:
1. Develop a basic Python Flask web application.
2. Containerize the Flask app using Docker.
3. Set up an AWS EC2 instance and install Docker.
4. Use GitHub Actions to automate:
   - Building the Docker image.
   - Pushing the image to a Docker registry.
   - Deploying the image to the EC2 instance.
5. Ensure the app is deployed and running in a Docker container on the EC2 instance using Docker Compose.

## Steps

### Step 1. Create a Basic Flask App
- Write a simple Flask app in Python.
- Push the code to this GitHub repository.

### Step 2. Create a Dockerfile
- Create a Dockerfile to containerize the Flask app.

### Step 3. Set Up an EC2 Instance & Install Docker
- Launch an AWS EC2 instance.
- SSH into the instance and install Docker:
```
sudo yum update -y
sudo yum install docker -y
sudo service docker start
sudo usermod -a -G docker ec2-user
```
### Step 4. Set Up GitHub Actions Workflow
- Create a GitHub Actions workflow to automate:
- Building the Docker image.
- Pushing the image to a Docker registry (e.g., Docker Hub).
- Deploying the container to the EC2 instance.

### Step 5. Use Docker Compose on EC2
- Create a docker-compose.yml file on your EC2 instance to manage the container.

### Step 6. Ensure the Container is Running
- After deployment, the Flask app should be running inside a Docker container on your EC2 instance. You can access it by navigating to the public IP of the EC2 instance.
```
  curl http://<ec2-public-ip>
```

## Conclusion
By following this guide, you've successfully built a CI/CD pipeline that automates the deployment of a containerized Python Flask app to an AWS EC2 instance using GitHub Actions and Docker.
