pipeline {
    agent none
    stages {
        stage('Build Docker Image') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh 'docker build -t desmo .'
                }
            }
        }
        stage('Deploy') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh 'docker rm -f $(docker ps -a -q)'
                    sh 'docker run -d -p 80:80 --name dolly desmo'
                    sh 'docker rmi $(docker images)' // remove all unused images
                }
            }
        }
    }
}