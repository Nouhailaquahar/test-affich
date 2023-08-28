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
                  sh 'npm cache clean --force'
                    sh 'npm install' //  Installer les dépendances
                    sh 'npm run build' // Compile le projet Angular
                    sh 'npm test' // Exécute les tests
                }
            }
        }
      stage('Debug') {
    steps {
        sh 'node -v'
        sh 'npm -v'
    }
}

    }
}
