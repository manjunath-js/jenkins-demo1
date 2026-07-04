pipeline {
    agent any

    environment {
        IMAGE_NAME = "manjunathjs/jenkins-demo"
        IMAGE_TAG = "latest"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        }

        stage('Push Image') {
            steps {
                echo 'Push stage'
            }
        }
    }
}