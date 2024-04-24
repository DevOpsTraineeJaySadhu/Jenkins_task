pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh 'docker build -t desmo .'
                    sh 'docker run -d  desmo'
                    sh 'docker rm -f $(docker ps -a -q)'
                    sh 'docker rmi $(docker images)'
                }
            }
        }
    }
}  