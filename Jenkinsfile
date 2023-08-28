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
        
        
        stage('Build and Test') {
            steps {
                script {
                    sh 'npm run install'
                }
            }
        }
        
      
    }
}
