pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build 'PES1UG21CS052-1'
                    sh 'g++ -o main/output main/main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Add execution permission and run the compiled C++ program
                    sh 'chmod +x main/output'
                    sh './main/output'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'deploy'
                    // Add deployment steps if needed
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed.'
        }
    }
}

