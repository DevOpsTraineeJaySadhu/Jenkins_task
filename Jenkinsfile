pipeline {
    agent any
     stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t desmo .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d --name demqo desmo'
                }
            }
        }
    }
}