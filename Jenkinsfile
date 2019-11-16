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
        bat(script: 'set', returnStatus: true)
      }
    }

  }
}