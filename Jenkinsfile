pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh 'docker rmi $(docker images)'
                    sh 'docker build -t desmo .'
                    sh 'docker images'
                    sh 'docker run -d  -p 80:80 --name dolly desmo'
                    sh 'docker ps'
                    sh 'docker rm -f $(docker ps -a -q)'
                    
                }
            }
        }
    }
}  