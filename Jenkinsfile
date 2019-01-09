pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t localhost:5000/${IMAGE_NAME}:${BUILD_NUMBER} .'
      }
    }
    stage('Push Image') {
      steps {
        sh 'docker push localhost:5000/${IMAGE_NAME}:${BUILD_NUMBER}'
      }
    }
        stage('Pull') {
      steps {
        sh 'curl -X POST http://192.168.79.83:8080/pull'
      }
    }
}
}
