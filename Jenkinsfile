pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Cette étape est effectuée par défaut lorsque vous choisissez "Pipeline script from SCM"
                checkout scm
            }
        }
        stage('Build') {
            steps {
              dir('\\affiche-test'){
                sh 'npm install'
                sh 'npm run build'
              }
            }
        }
        stage('Deploy') {
            steps {
                // Exécutez ici les commandes pour déployer votre application Angular
                // Par exemple, si vous utilisez ng serve pour tester localement :
              
              dir('\\affiche-test'){
                sh 'ng serve &'
              }
            }
        }
        stage('Afficher un message') {
            steps {
                echo 'Le projet Angular a été construit et déployé avec succès !'
            }
        }
    }
}
