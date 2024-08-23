pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Pranalipokharkar/Jenkins.git', branch: 'main'
            }
        }
        
        stage('Stage1') {
            steps {
                echo "Welcome to stage1"
            }
        }
        
        stage('Stage2') {
            steps {
                echo "Welcome to stage2"
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

