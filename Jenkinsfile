pipeline {
    agent any
    environment {
        GIT_REPO = 'https://github.com/MayankSharma247/March14.git'
        EMAIL_RECIPIENTS = 'mayanksharma247@gmail.com'  // Replace with your email
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
        success {
            emailext (
                to: "${EMAIL_RECIPIENTS}",
                subject: "Jenkins Build Success: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "The build for ${env.JOB_NAME} #${env.BUILD_NUMBER} was successful."
            )
        }
        failure {
            emailext (
                to: "${EMAIL_RECIPIENTS}",
                subject: "Jenkins Build Failure: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                body: "The build for ${env.JOB_NAME} #${env.BUILD_NUMBER} has failed. Please check the Jenkins logs for more details."
            )
        }
        always {
            echo 'Application running successfully!'
        }
    }
}
