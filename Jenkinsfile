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
                sh 'output'
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
