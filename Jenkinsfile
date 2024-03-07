pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build 'PES1UG21CS052-1'
                sh 'g++ -o main/output main/main.cpp'
            }
        }
        stage('Test') {
            steps {
                sh 'chmod +x main/output'
                sh './main/output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed.'
        }
    }
}

