//SCRIPTED

//DECLARATIVE
pipeline {
    agent any
    //agent { docker { image 'maven:3.6.3'} }
    environment {
       dockerHome = tool 'myDocker'
       mavenHome = tool 'myMaven'
       PATH = "$dockerHome/bin:$mavenHome:bin:$PATH"
    }
    stages {
         stage('Checkout'){
             steps {
                //sh 'mvn --version'
                sh 'docker version'
 		echo "Build"
                echo "$PATH"
                echo "BUILD NUMBER - $env.BUILD_NUMBER"
                echo "BUILD ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
            }
          }
         stage('Compile'){
             steps {
                 sh "mvn clean complete"
            }
         }
          stage('Test'){
             steps {
 		echo "Test"
                sh "mvn test"
             }
          }
          stage('Integration Testing'){
             steps {
 		echo "Integration Test"
                sh "mvn failsafe:integration-test failsafe:verify"
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