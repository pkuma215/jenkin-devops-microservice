//SCRIPTED

//DECLARATIVE
pipeline {
    //agent any
    agent { docker { image 'maven:3.6.3'} }
    stages {
         stage('Build'){
             steps {
                sh 'mvn --version'
 		echo "Build"
            }
          }
          stage('Test'){
             steps {
 		echo "Test"
             }
          }
          stage('Integration Testing'){
             steps {
 		echo "Integration Test"
             }
          }
     } 
     post {
          always {
            echo 'i am always runs'
          }
          success {
            echo 'i run when you are successful' 
          }
          failure {
            echo 'i run when you fail'
          }
   
    }
}