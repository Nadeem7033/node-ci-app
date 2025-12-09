pipeline {
    agent any

    tools {
        nodejs "node18"         // Name of Node.js installation in Jenkins
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Nadeem7033/node-ci-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo "Build Step (Node apps usually don’t need build unless using TypeScript)"
            }
        }

        stage('Start App') {
            steps {
                sh 'npm start &'
            }
        }
    }
}
