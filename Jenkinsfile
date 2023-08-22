pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build and Display Message') {
            steps {
                sh 'npm install'
                sh 'npm run build'
                echo 'Le pipeline a construit avec succès le projet Angular et voici votre message : Bonjour depuis Jenkins !'
            }
        }
    }
}
