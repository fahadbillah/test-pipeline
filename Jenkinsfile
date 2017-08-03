pipeline {
  agent any
  node('master') {
    stages {
      stage('Build') {
        steps {
          echo 'Start building...'
          sh 'touch README.md'
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
}