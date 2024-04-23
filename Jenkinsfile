pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository and clone only the specific directory
                git url: 'https://github.com/DevOpsTraineeJaySadhu/Jenkins_task.git', 
                    branch: 'demo'
            }
        }
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
    post {
        always {
            cleanWs()
        }
    }
}
