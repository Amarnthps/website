pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'docker build -t website-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application...'
            }
        }

        stage('Production') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying to Production...'
            }
        }
    }
}