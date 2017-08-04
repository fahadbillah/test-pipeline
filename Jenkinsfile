pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Start building...'
        sh 'touch README.md'
        writeFile file: 'README.md', text: '''# Pipeline Practice

        This pipeline is a practice one.'''
        def someText = readFile 'README.md'
        echo someText
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