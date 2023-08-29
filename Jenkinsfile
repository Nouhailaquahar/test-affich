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
                    sh 'npm install'
                }
            }
        }
        
        stage('Build and Test') {
    steps {
        script {
            bat 'npm run build' // Utilisation de "bat" pour exécuter des commandes Windows
        }
    }
}

        

    }
    
    post {
        always {
            echo 'This will always run'
        }
        
        success {
            echo 'This will run only if the build is successful'
        }
        
        failure {
            echo 'This will run only if the build fails'
        }
        
        unstable {
            echo 'This will run only if the build is unstable'
        }
        
        changed {
            echo 'This will run if the build is successful and the state has changed'
        }
    }
}
