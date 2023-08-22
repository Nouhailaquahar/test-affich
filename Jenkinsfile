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
                // Notez que vous n'avez pas besoin de "ng serve" ici
                // Effectuez le déploiement selon votre processus habituel
            }
        }
    }
}
