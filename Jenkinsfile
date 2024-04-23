pipeline {
    agent any
    
    stages {
        stage('Print Working Directory') {
            steps {
                sh 'pwd'
            }
        }
        stage('List Directory Contents') {
            steps {
                sh 'ls'
            }
        }
    }
    
    post {
        success {
            // Actions to perform if the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if the
