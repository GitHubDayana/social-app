pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/saiprasadr870/social-app'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm run'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here (For example, starting the server)
                sh 'nohup npm start &'
            }
        }
    }
    post {
        success {
            echo 'Application deployed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
