pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'docker build -t ganesh077/automation:latest .'
      }
    }
    stage('Push') {
      steps {
        withCredentials([usernamePassword(credentialsId: 'ganesh077', passwordVariable: 'DOCKERHUB_PASS', usernameVariable: 'DOCKERHUB_USER')]) {
          sh 'docker login -u ganesh077 -p (cqrA8pPS(&M*$K'
          sh 'docker push ganesh077/automation:latest'
        }
      }
    }
  }
}
