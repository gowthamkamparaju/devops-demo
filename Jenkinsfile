pipeline {
    agent any
 
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t gowthamkamparaju/devops-demo:v1 .'
            }
        }
 
        stage('Trivy Scan') {
            steps {
                sh 'trivy image gowthamkamparaju/devops-demo:v1 || true'
            }
        }
 
        stage('Push Docker Image') {
            steps {
                sh 'docker push gowthamkamparaju/devops-demo:v1'
            }
        }
    }
}
