# Kubernetes CI/CD Pipeline Project

## Overview
This project demonstrates an end-to-end CI/CD pipeline using Jenkins, Docker, Kubernetes, GitHub, and AWS.

## Tech Stack
- AWS EC2
- Jenkins
- Docker
- Kubernetes
- GitHub
- DockerHub

## Workflow
1. Developer pushes code to GitHub
2. Jenkins pulls latest code
3. Docker image is built
4. Docker image is pushed to DockerHub
5. Kubernetes deployment is updated automatically

## Kubernetes Architecture
- 1 Master Node
- 2 Worker Nodes
- Deployment
- NodePort Service

## Verification
- Jenkins pipeline successful
- Pods running across worker nodes
- Website accessible through NodePort

