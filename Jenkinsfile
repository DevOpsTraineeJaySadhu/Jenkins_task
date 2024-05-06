pipeline {
    agent any
    
    stages {
        stage('Check Branch') {
            steps {
                script {
                    // Get the current branch name
                    def branchName = env.BRANCH_NAME ?: 'unknown'
                    
                    // Check the branch and execute commands accordingly
                    if (branchName == 'main') {
                        echo 'hello i am from main branch'
                    } else if (branchName == 'stage') {
                        echo 'hello i am from stage branch'
                    } else {
                        echo 'hello i am from Nowhere'
                    }
                }
            }
        }
    }
}
