pipeline {
    agent any
    
    environment {
        NODEJS_HOME = tool(name: 'nodejs', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation')
        PATH = "${NODEJS_HOME}/bin:${PATH}"
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Installer les dépendances Node.js
                bat label: 'Install Dependencies', script: 'npm install'
            }
        }
        
        stage('Build and Test') {
            steps {
                script {
                    def buildResult = bat label: 'Build', script: 'npm run build', returnStatus: true
                    def testResult = bat label: 'Test', script: 'npm test', returnStatus: true
                    if (buildResult == 0 && testResult == 0) {
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
            echo 'Le pipeline a été exécuté avec succès!'
        }
    }
}
