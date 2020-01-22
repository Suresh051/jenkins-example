pipeline {
    agent any
   
    stages {
        stage ('Compile Stage') {
            def mvnHome = tool name: 'maven-3', type: 'maven'
             def mvnCMD = "${mvnHome}/bin/mvn"
            steps {
                
                sh "${mvnCMD} clean compile"
            }
        }

        stage ('Testing Stage') {
 def mvnHome = tool name: 'maven-3', type: 'maven'
   def mvnCMD = "${mvnHome}/bin/mvn"
            steps {
             
               sh "${mvnCMD} test"
            }
        }


        stage ('Deployment Stage') {
             def mvnHome = tool name: 'maven-3', type: 'maven'
   def mvnCMD = "${mvnHome}/bin/mvn"
            steps {
             
                sh "${mvnCMD} deploy"
            }
        }
    }
}
