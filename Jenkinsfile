pipeline {
    agent any
   
   tools {
        maven 'maven-3'
        jdk 'Java'
    }
    stages {
        stage ('Compile Stage') {
            
            steps {
                
                sh "mvn clean compile"
            }
        }

        stage ('Testing Stage') {

            steps {
             
               sh "mvn test"
            }
        }


        stage ('Deployment Stage') {
       
            steps {
             
                sh "mvn deploy"
            }
        }
    }
}
