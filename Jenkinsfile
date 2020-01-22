pipeline {
    agent any
   
    environment {
        def mvnHome = tool name: 'maven-3', type: 'maven'
             def mvnCMD = "${mvnHome}/bin/mvn"
    }
    stages {
        stage ('Compile Stage') {
            
            steps {
                
                sh "${mvnCMD} clean compile"
            }
        }

        stage ('Testing Stage') {

            steps {
             
               sh "${mvnCMD} test"
            }
        }


        stage ('Deployment Stage') {
       
            steps {
             
                sh "${mvnCMD} deploy"
            }
        }
    }
}
