pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Start building...'
        sh 'touch README.md'
        writeFile file: 'README.md', text: '''# Pipeline Practice

        This pipeline is a practice one.'''
        env.WORKSPACE = pwd()
        def version = readFile "${env.WORKSPACE}/README.md"
        echo version
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