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
                // Intentional error - using a non-existing file
                sh './non_existing_file'
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

