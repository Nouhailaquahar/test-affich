pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ng serve '
            }
        }
        stage('Afficher un message') {
            steps {
                echo 'Le projet Angular a été construit et déployé avec succès !'
            }
        }
    }
}
