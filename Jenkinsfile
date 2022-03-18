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
     withCredentials([string(credentialsId: 'DOCKER_HUB_CREDENTIALS', variable: 'DOCKERHUB')]) {
     sh "docker login -u kavithasake -p ${DOCKER_HUB_CREDENTIALS}"
     sh "docker tag cmr-repo/myapp:1.0 kavithasake/cmr:1.0"
     sh "docker push kavithasake/cmr:1.0"
            }
        }
   }
}
 
   
    
        
                        
                          
                          
                          
                          
                          
                          
                          
                          
                          
