pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Récupérer le code source du référentiel Git
                checkout scm
            }
        }
        
        stage('Build and Test') {
            steps {
                // Exécution des étapes de build et de test (remplacez ces commandes par celles de votre projet)
                sh 'npm install'
                sh 'npm run build'
                sh 'npm test'
            }
        }
    }
    
    post {
        always {
            // Afficher un message à la fin du pipeline
            echo 'Le pipeline a été exécuté avec succès!'
        }
    }
}
