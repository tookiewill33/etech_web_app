pipeline {
agent any 
  stages{
    stage('git-clone'){
      steps {
      checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'cicd', url: 'https://github.com/tookiewill33/etech_web_app.git']])
    }
    }
    stage('check-user'){
      steps{
        sh ' cat /etc/passwd '
      }
    } 
  }
}
   
