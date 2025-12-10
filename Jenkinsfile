pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo "Build step completed"
            }
        }

        stage('Deploy') {
            steps {
                echo "App is ready for deployment (not starting server in pipeline)"
            }
        }
    }
}
