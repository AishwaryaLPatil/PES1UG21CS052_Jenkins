pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file
                sh 'g++ -o main/output main/main.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print output of the compiled C++ program
                script {
                    def output = sh(script: './main/output', returnStdout: true).trim()
                    echo "Output of the C++ program: ${output}"
                }
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

