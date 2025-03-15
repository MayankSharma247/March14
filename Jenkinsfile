pipeline {
    agent any
    environment {
        GIT_REPO = 'https://github.com/MayankSharma247/March14.git'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying project...'
            }
        }
    }
    post {
        always {
            echo 'Notification sent!'
        }
    }
}
