pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the repository'
                git branch: 'main', url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Flask application'
                // Example build command (You can add your own commands here)
                sh 'pip install -r requirements.txt'  // Installing dependencies
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                // You can replace the following line with a real test command
                sh 'pytest tests/'  // Run your tests with pytest or any other test tool
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the Flask app'
                // Replace with real deployment steps (optional)
                // For example, deploy to AWS, Heroku, etc.
            }
        }

        stage('Notification') {
            steps {
                echo 'Notifying success or failure'
                // You can add steps for notifications (e.g., sending an email)
                // For example, `mail` or `Slack` notifications
            }
        }
    }
}
