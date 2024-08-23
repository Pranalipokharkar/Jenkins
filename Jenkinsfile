pipeline {
    agent any

    stages {
        stage('Stage1') {
            steps {
                echo "Welcome to stage1"
            }
        }
            
        stage( 'Stage2' ) {
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
