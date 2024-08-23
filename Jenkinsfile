pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Stage1') {
            steps {
                echo "Welcome to stage1"
            }
        }
        
    }

    post {
        // Steps to run at the end of the pipeline
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}

