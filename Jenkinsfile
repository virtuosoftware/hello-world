pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'hello world!'
      }
    }

    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        bat(script: './docker.bat', returnStatus: true)
      }
    }

  }
}