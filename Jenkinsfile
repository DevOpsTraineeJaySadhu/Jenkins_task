pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh 'docker build -t desmo .'
                }
            }
        }
        
        stage('Deploy') {
            agent {
                label "slave"
            }
            steps {
                script {
                    sh '''
                        containers=$(docker ps -a -q)
                        if [ -n "$containers" ]; then
                            docker rm -f $containers
                        fi
                    '''
                    sh 'docker run -d -p 80:80 --name dolly desmo'
                    sh 'docker image prune -a -f' // remove all unused images
                }
            }
        }
    }
    // post {
    //     always { 
    //         script {
    //             cleanWs()
    //        }
    //     }
    // }
}
