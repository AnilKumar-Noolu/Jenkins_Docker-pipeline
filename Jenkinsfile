pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        sh 'docker build -t anilkumarnooludocker/jenkinsdemo:"$BUILD_ID" .'
      }
    }
    stage('publish'){
      steps{
        withDockerRegistry(credentialsId: "dockerhub", url: "")
        sh 'docker push anilkumarnooludocker/jenkinsdemo:"$BUILD_ID" '
      }
    }
  }
}
    
