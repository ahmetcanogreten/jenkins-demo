pipeline {
    agent any

    stages{
        stage("build") {
            steps {
                echo 'Building the application...'
            }
        }

        stage("test") {
            when {
                expression {
                    BRANCH_NAME == 'main2'
                }
            }
            steps {
                echo 'Testing the application...'
            }
        }

        stage("deploy") {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        always {
            echo 'Post-processing...'
        }

        success {
            echo 'Post-processing on success...'
        }

        failure {
            echo 'Post-processing on failure...'
        }
    }
}