pipeline {
    agent any
    stages {
        stage('Build and Run Docker Image') {
            steps {
                script {
                    sh 'docker build -t demo .'
                    sh 'docker run -d --name demofor demo'
                    echo "Docker image created and container started successfully"
                }
            }
        }
    }
}