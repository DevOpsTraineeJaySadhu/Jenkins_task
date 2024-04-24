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
                    sh 'docker run -d  -p 80:80 --name dolly desmo'
                    sh 'docker rm -f $(docker ps -a -q)'
                    sh 'docker rmi $(docker images)'
                }
            }
        }
    }
}  