pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/gaurav2311gehu/flask-k8s-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("flask-k8s-app")
                }
            }
        }

        stage('Push Image to Docker Hub') {
            steps {
                withDockerRegistry([ credentialsId: 'dockerhub-creds', url: '' ]) {
                    script {
                        docker.image("flask-k8s-app").push('latest')
                    }
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}
