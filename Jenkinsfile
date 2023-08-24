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
                script {
                    def installResult = sh(script: 'npm install', returnStatus: true)
                    def buildResult = sh(script: 'npm run build', returnStatus: true)
                    def testResult = sh(script: 'npm test', returnStatus: true)
                    
                    if (installResult == 0 && buildResult == 0 && testResult == 0) {
                        currentBuild.result = 'SUCCESS'
                    } else {
                        currentBuild.result = 'FAILURE'
                    }
                }
            }
        }
    }
    
    post {
        success {
            // Afficher un message à la fin du pipeline en cas de succès
            echo 'Le pipeline a été exécuté avec succès!'
        }
    }
}
