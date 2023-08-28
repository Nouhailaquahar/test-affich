pipeline {
    agent any
    
    tools {
        nodejs '16.13.0'
    }
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }
        
        stage('Build and Test') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        
    }
}
