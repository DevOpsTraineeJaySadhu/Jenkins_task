pipeline {
    agent any
    stages {
        stage('Print Working Directory') {
            steps {
                script {
                    sh 'docker build -t demo .'
                    sh 'docker run -d --name demofor demo'
                    echo "Images created successfully"
                }
            }
    }
}