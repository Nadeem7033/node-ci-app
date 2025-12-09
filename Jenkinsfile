pipeline {
    agent any

    tools {
        nodejs "node18"
    }

    stages {
        stage('Checkout Code') {
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
                bat 'echo "Build step completed"'
            }
        }

        stage('Start App') {
            steps {
                bat 'node index.js'
            }
        }
    }
}

