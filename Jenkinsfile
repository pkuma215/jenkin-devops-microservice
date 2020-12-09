//SCRIPTED

//DECLARATIVE
pipeline {
    agent any
    stages {
         stage('Build'){
             steps {
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