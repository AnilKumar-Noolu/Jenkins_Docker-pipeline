pipeline{
  agent any
  stages{
    stage('env'){
      steps{
        sh 'printenv'
        sh 'git version'
      }
    }



    stage('build'){
      st
        sh 'docker build -t anilkumarnooludocker/jenkinsdemo:"$BUILD_ID" .'
      }
    }
    stage('publish'){
      steps{
        withDockerRegistry([credentialsId: "dockerhub", url: ""]){

          sh 'docker push anilkumarnooludocker/jenkinsdemo:"$BUILD_ID" '
        }
      }
    }
  }
}
    
