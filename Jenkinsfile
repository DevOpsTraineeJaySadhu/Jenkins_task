pipeline {
    agent any
     stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-docker-image:latest', 'Dockerfile')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('my-docker-image:latest').run('--name my-container -d ')
                }
            }
        }
    }
}