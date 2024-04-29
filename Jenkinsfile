pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the repository
                git branch: 'main', url: 'https://github.com/ragul-tickey/demo.git'
            }
        }

        stage('Build') {
            steps {
                // Build your frontend application
                sh 'npm install' // or whatever command you use to build your app
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application
                sh 'scp -r /var/www/html/* user@server:/var/www/html/'
            }
        }
    }
}
