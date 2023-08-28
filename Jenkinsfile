pipeline {
    agent any
    
    tools {
        nodejs '18.17.0'
    }
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }
        
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm ci'
                }
            }
        }
        
        stage('Build and Test') {
            steps {
                script {
                    sh 'npm run build'
                    sh 'npm test'
                }
            }
        }
        
      
    }
}
