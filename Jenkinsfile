pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh 'echo \'Checkout stage\''
      }
    }
    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            sh 'echo \'Run unit test\''
          }
        }
        stage('Cucumber Test') {
          steps {
            sh 'echo \'Run cucumber reports\''
          }
        }
      }
    }
    stage('Deploy to QA') {
      steps {
        sh 'echo \'Deploy to QA'
      }
    }
  }
}