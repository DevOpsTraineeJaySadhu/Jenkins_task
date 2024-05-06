pipeline {
    agent any
    
    stages {
        stage('Check Branch') {
            steps {
                script {
                    // Get the current branch name
                    def branchName = env.BRANCH_NAME ?: 'main'
                    
                    // Check the branch and execute commands accordingly
                    if (branchName == 'main') {
                        echo 'hello i am from main branch'
                    } else if (branchName == 'demo') {
                        echo 'hello i am from demo branch'
                       } else if (branchName == 'xyz') {
                        echo 'hello i am from xyz branch'
                    } else {
                        echo 'hello i am from Nowhere'
                    }
                }
            }
        }
    }
}
