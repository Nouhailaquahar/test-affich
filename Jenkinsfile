
pipeline {
    agent any
    
    tools {
        nodejs '18.17.0'
    }
    
    stages {  
       stage("Clone Git Repository") {
            steps {
                git(
                    url: "https://github.com/Nouhailaquahar/test-affich.git",
                    branch: "main",
                    changelog: true,
                    poll: true
                )
            }
        }
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
                    sh 'npm install --verbose'
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
