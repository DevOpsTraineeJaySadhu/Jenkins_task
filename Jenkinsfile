pipeline {
    agent any
    stages {
        stage('Build and Run Docker Image') {
            steps {
                script {
                    docker.build('demo','Dockerfile')
                    docker.image('demo').run('-d --name demofor')
                    echo "Docker image created and container started successfully"
                }
            }
        }
    }
}