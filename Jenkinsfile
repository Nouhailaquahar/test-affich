
pipeline {
    agent any
    
    tools {
        nodejs '18.17.0'
    }
    
    stages {  
       stage('Checkout') {
            steps {
                script {
                    checkout scm
                  echo'le code bien recupére du git'
                }
            }
        }
    
    }
}
