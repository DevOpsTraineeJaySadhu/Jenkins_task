pipeline {
    agent any
    stages {
        stage('Print Working Directory') {
            steps {
                sh 'pwd'
            }
        }
        stage('Print Working Directory') {
            steps {
                sh 'ls'
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if the pipeline fails
        }
    }
}