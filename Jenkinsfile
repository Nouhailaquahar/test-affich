
pipeline {
    agent any // Utilise n'importe quel agent disponible pour exécuter le pipeline

    stages {
        stage('Checkout') { // Étape de récupération du code source depuis Git
            steps {
                checkout scm
            }
        }
        stage('Build') { // Étape de construction de votre application
            steps {
                sh 'npm install' // Exemple: Installation des dépendances pour un projet Node.js
                sh 'npm run build' // Exemple: Compilation de l'application
            }
        }
        stage('Test') { // Étape de tests
            steps {
                sh 'npm test' // Exemple: Exécution des tests unitaires
            }
        }
        stage('Deploy') { // Étape de déploiement
            steps {
                sh 'npm deploy' // Exemple: Déploiement de l'application
            }
        }
    }
}
