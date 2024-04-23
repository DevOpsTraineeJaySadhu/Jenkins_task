pipeline {
    agent any
    stages {
        stage('Build and Run Docker Image') {
            steps {
                script {
                    sh 'sudo docker build -t demo .'
                    sh 'sudo docker run -d --name demofor demo'
                    echo "Docker image created and container started successfully"
                }
            }
        }
    }
}