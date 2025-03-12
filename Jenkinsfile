pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/SanjayaSankar/PES2UG22CS502_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './output'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
