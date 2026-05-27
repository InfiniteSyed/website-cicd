pipeline {
    agent any

    environment {
        IMAGE_NAME = "syedashu/website:v1"
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/InfiniteSyed/website-cicd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

        stage('Deploy To Kubernetes') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }
    }
}
