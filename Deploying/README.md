# Web Application CI/CD Pipeline

This repository contains a simple web application and a CI/CD pipeline setup using Git, Ansible, Docker, Kubernetes, and Jenkins.

## Project Structure
webapp/
├── index.html
├── Dockerfile
├── deployment.yml
├── deploy.yml
└── Jenkinsfile


- `index.html`: A simple web application.
- `Dockerfile`: Dockerfile to build the Docker image.
- `deployment.yml`: Kubernetes deployment configuration.
- `deploy.yml`: Ansible playbook to deploy the web application.
- `Jenkinsfile`: Jenkins pipeline script.

## Setup Instructions

### Step 1: Clone Repository

- Clone this repository to your local machine:

- git clone https://github.com/Nashat-Ahmed/simpleCI-CD.git

- cd wepapp

### Run The Playbook
- ansible-playbook deploy.yml

### Build The Docker image
- docker build -t your-dockerhub-username/webapp .

### Pushing The Image Docker Hub
- docker login
- docker push your-dockerhub-username/webapp

### Apply The Deployment
- kubectl apply -f deployment.yml

### Expose The Deployment
- kubectl expose deployment webapp-deployment --type=LoadBalancer --port=80


### Automate the build and deployment process using Jenkins 
- create a new pipeline job and configure the pipeline script (Jenkinsfile)


