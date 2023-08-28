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
                    sh 'npm install' // Utilisation de la commande correcte pour installer les dépendances
                    sh 'npm run build' // Compile le projet Angular
                    sh 'npm test' // Exécute les tests
                }
            }
        }
    }
}
