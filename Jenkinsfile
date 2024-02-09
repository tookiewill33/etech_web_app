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
        sh ' cat /etc/shadow '
        sh ' grep jenkins /etc/passwd '
        sh ' ls -a '
      }
    }
    stage('add a new group'){
      steps{
        sh ' groupadd yvanfamily '
      }
    }
  }
}
   
