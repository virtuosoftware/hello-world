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
        sh 'echo \'docker test\''
      }
    }

  }
}