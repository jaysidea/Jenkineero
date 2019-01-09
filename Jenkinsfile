pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t localhost:5000/eero .'
      }
    }
    stage('Push Image') {
      steps {
        sh 'docker push localhost:5000/eero .'
      }
    }
        stage('Pull') {
      steps {
        sh 'curl -X POST http://192.168.79.83:8080/pull'
      }
    }
}
}
