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
        sh 'npm install'    // Installe les dépendances du projet
        sh 'npm run build'  // Exécute la commande de build (compilation) du projet
        sh 'npm test'       // Exécute les tests unitaires du projet
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
