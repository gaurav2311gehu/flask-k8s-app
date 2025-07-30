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
                bat 'docker build -t flask-k8s-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                echo 'Docker push step goes here'
                // bat 'docker login' and bat 'docker push ...' if needed
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s/'
            }
        }
    }
}
