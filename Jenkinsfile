pipeline {
  agent any
  stages {
    stage('Build') {
      node('master'){
        steps {
          echo 'Start building...'
          sh 'touch README.md'
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Start testing...'
      }
    }
    stage('Publish') {
      steps {
        echo 'Start publishing...'
      }
    }
  }
}