pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'hello world!'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          environment {
            CI = 'true'
          }
          steps {
            bat(script: 'set', returnStatus: true)
          }
        }

        stage('NPM version') {
          steps {
            bat(script: 'npm --version', returnStatus: true)
          }
        }

        stage('Docker version') {
          steps {
            bat(script: 'docker --version', returnStatus: true)
          }
        }

      }
    }

  }
}