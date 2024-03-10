pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS266-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Display') {
      steps {
        echo "Deployment successful";
      }
    }
  }
  post {
failure {
  error 'Pipeline Failed'
}
  }
}
