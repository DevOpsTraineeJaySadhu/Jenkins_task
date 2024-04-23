pipeline {
    agent any
    stages {
        stage('Print Working Directory') {
            steps {
                script {
                    sh 'pwd'
                    echo "Current working directory: ${pwd()}"
                }
            }
        }
        stage('List Files') {
            steps {
                script {
                    sh 'ls'
                    echo "Files in the current directory: ${ls()}"
                }
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