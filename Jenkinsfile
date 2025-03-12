pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage...'
                sh 'g++ -o output main.cpp || exit 1'
            }
        }

        stage('Test') {
            steps {
                echo 'Starting Test Stage...'
                sh 'chmod +x output && ./output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed successfully'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Please check the logs for errors.'
        }
    }
}
