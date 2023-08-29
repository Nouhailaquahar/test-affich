




pipeline {
    agent any
    
    tools {
        nodejs '18.17.0'
    }
    
    stages {  
        stage('Build and Test') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        
        stage('Run Angular Project') {
            steps {
                script {
                    sh 'npm run start' 
                }
            }
        }
    }
}
