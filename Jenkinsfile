pipeline {
 agent any
 stages{
  stages("Git checkout"){
   steps{
    withCredentials([gituserPassword(credentialsId: '17928343-3100-4a2b-87ac-a6bf5db28c61',gitToolName: 'git')]) {
       }
    }
  }
  stage("maven clean build"){
    steps{
        sh "mvn clean package"
        }
      }
  stage("Building Docker image"){
   steps{
     sh "docker build -t cmr-repo/myapp:1.0 ."
    
        
                        
                          
                          
                          
                          
                          
                          
                          
                          
                          
