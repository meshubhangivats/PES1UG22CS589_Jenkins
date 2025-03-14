pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ main.cpp -o output || exit 1'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo "deploy.."
            }
        }
    }
    post{
        failure {
            echo 'Pipeline failed'
        }
    }
}
