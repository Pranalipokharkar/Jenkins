pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "pranali2482/myimage:${BUILD_NUMBER}"
        REGISTRY_CREDENTIALS = credentials('docker-cred')
    }

    stages {
        stage('Checkout Code') {
            steps {
                // Assuming you're using Git
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t ${DOCKER_IMAGE} .'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    def dockerImage = docker.image("${DOCKER_IMAGE}")
                    docker.withRegistry('https://index.docker.io/v1/', "${REGISTRY_CREDENTIALS}") {
                        dockerImage.push()
                    }
                }
            }
        }

    }
 }

   
}
