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

        stage('Verify Step') {
          steps {
            input(message: 'Finished using the web site? (Click "Proceed" to continue)', id: '1')
          }
        }

      }
    }

  }
}