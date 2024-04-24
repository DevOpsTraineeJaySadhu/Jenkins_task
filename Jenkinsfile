pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            agent {
                label "ubuntu(slave-jay)"
            }
            steps {
                script {
                    sh 'docker build -t desmo .'
                    sh 'docker run -d --name demqo desmo'
                }
            }
        }
    }
}