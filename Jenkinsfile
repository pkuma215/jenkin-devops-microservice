//SCRIPTED

//DECLARATIVE
pipeline {
    agent any
    //agent { docker { image 'maven:3.6.3'} }
    stages {
         stage('Build'){
             steps {
                //sh 'mvn --version'
 		echo "Build"
                echo "$PATH"
                echo "BUILD NUMBER - $env.BUILD_NUMBER"
                echo "BUILD ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
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