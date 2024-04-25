pipeline {
    agent any
    stages {
        stage('Delete Workspace') {
            steps {
                script {
                    dir('/var/lib/jenkins/workspace') {
                        sh 'rm -rf *'
                    }
               }
            }
        }
    }
}
