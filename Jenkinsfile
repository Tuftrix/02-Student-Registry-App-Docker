pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
              echo 'Checking out code from Git'
            }
        }

        stage('Setup Node.js') {
            steps {
                echo 'Setting up Node.js'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Start Application') {
            steps {
                echo 'Starting application'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Build and tests ran successfully!'
        }
        failure {
            echo 'Something went wrong! Check logs.'
        }
    }
}
