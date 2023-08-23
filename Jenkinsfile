pipeline {
    agent any
    
    environment {
        NODEJS_VERSION = '18.17.0' // La version de Node.js que vous avez configurée dans Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Configuration de Node.js
                tools {
                    nodejs "${NODEJS_VERSION}"
                }
                script {
                    sh 'npm install'
                }
            }
        }
        
        stage('Build and Test') {
            steps {
                script {
                    sh 'npm run build' // Exécute la commande de build d'Angular
                    sh 'npm test'      // Exécute les tests unitaires
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Ici, vous pourriez mettre en place le déploiement de votre application
                // vers un serveur ou une plateforme de déploiement.
                // Cela dépend de votre infrastructure et de vos besoins.
            }
        }
    }
    
    post {
        always {
            // Archivage des artefacts (par exemple, les fichiers de build) pour référence future
            archiveArtifacts artifacts: '**/dist/**', allowEmptyArchive: true
            
            // Génération du rapport d'affichage ou d'autres notifications
            // selon la manière dont vous souhaitez afficher les résultats.
            // Cela pourrait être des notifications par e-mail, des notifications Slack, etc.
        }
    }
}
