pipeline {
    agent any
    stages {
        stage('Delete Workspace') {
            steps {
                script {
                    dir('cd /var/lib/jenkins/workspace') {
                        sh 'sudo rm -rf *'
                    }
               }
            }
        }
    }
}
