pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // build 'PES1UG21CS052-1'
                sh 'g++ -o output main.cpp'
            }
        }
        stage('Test') {
            steps {
                // Run the compiled C++ program
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps if needed
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed.'
        }
    }
}

