pipeline {
    agent any
tools {
   nodejs '18.17.0' 
}
    stages {
     /*   stage('Checkout') {
            steps {
                // Cette étape est effectuée par défaut lorsque vous choisissez "Pipeline script from SCM"
                checkout scm
            }
        }
        stage('Build') {
            steps {
              dir('\\src'){
                sh 'npm install'
                sh 'npm run build'
              }
            }
        }*/
        stage('Deploy') {
            steps {
              script{
                // Exécutez ici les commandes pour déployer votre application Angular
                // Par exemple, si vous utilisez ng serve pour tester localement :
              
              dir('\\src'){
                sh 'npm run start'
              }
            }
            }
        }
       // stage('Afficher un message') {
         //   steps {
             //   echo 'Le projet Angular a été construit et déployé avec succès !'
           // }
        //}
    }
}
