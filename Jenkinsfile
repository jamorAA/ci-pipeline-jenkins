pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                echo 'testing the application...'
                echo "executing pipeline for branch $BRANCH_NAME"
            }
        }
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == 'feature/test-multibranch-pipeline-1'
                }
            }
            steps {
                echo 'building the application...'
            }
        }
        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == 'feature/test-multibranch-pipeline-1'
                }
            }
            steps {
                echo 'deploying the application...'
            }
        }
    }
}