pipeline {
    agent any

    stages {
        stage('Afficher Bonjour') {
            steps {
                echo 'Bonjour, ceci est un exemple de pipeline Jenkins !'
            }
        }
        stage('Build and Deploy') {
            steps {
                sh 'npm install' // Installer les dépendances
                sh 'npm run build' // Compiler le projet Angular
                sh 'npm deploy' // Déployer le projet (ajustez en fonction de votre configuration)
            }
        }
    }
}
