pipeline {
agent any 
  stages{
    stage('git-clone'){
      steps {
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/tookiewill33/etech_web_app']]])
    }
    }
    stage('check-user'){
      steps{
        sh ' cat /etc/passwd '
      }
    }
    stage('add a new user'){
      steps{
        sh ' useradd yvanfamily '
      }
    }
  }
}
   
