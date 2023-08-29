pipeline {
    agent any
    
    stages {
      tage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }
        stage('Build and Test') {
            steps {
                script {
                    def npmPath = 'C:\\Users\\HP 840 G3\\AppData\\Roaming\\npm'
                    sh "${npmPath}\\npm install"
                }
            }
        }
    }
}
