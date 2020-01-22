pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                def mvnHome = tool name: 'maven-3', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                sh "${mvnCMD} clean compile"
            }
        }

        stage ('Testing Stage') {

            steps {
               def mvnHome = tool name: 'maven-3', type: 'maven'
               def mvnCMD = "${mvnHome}/bin/mvn"
               sh "${mvnCMD} test"
            }
        }


        stage ('Deployment Stage') {
            steps {
                def mvnHome = tool name: 'maven-3', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                sh "${mvnCMD} deploy"
            }
        }
    }
}
