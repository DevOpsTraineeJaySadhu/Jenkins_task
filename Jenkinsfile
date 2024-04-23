pipeline {
    agent any
    stages {
        stage('Print Working Directory') {
            steps {
                script {
                    def workingDir = pwd()
                    echo "Current working directory: ${workingDir}"
                }
            }
        }
        stage('List Files') {
            steps {
                script {
                    def files = sh(script: 'ls', returnStdout: true).trim()
                    echo "Files in the current directory: ${files}"
                    echo "Hello from Jay"
                }
            }
        }
    }
}