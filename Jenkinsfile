pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                
                build 'PES2UG22CS609'
                
                
                sh 'g++ -o output main.cpp'
            }
        }
        
        stage('Test') {
            steps {
                
                sh './output'
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
            error 'Pipeline failed'
        }
    }
}
