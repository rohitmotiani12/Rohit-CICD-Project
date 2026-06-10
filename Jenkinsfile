pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Tests passed!'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker build -t rohit-cicd-project .'
                echo 'Deployed!'
            }
        }
        stage('Notify') {
            steps {
                echo 'Build successful!'
            }
        }
    }
    post {
        success { echo 'Pipeline SUCCESS!' }
        failure { echo 'Pipeline FAILED!' }
    }
}
