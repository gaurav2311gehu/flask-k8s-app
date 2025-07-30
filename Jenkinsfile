pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/gaurav2311gehu/flask-k8s-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-k8s-app .'
            }
        }
        stage('Push Docker Image') {
            steps {
                echo 'Skipping for now or add Docker Hub login and push logic'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}
