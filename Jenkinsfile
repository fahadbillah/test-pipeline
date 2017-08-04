pipeline {
  agent any
  environment {
    FOO = "foo"
    PROP = readJSON file: '${WORKSPACE}/properties.json'
    project_title = PROP['project_title']
  }
  stages {
    stage('Build') {
      steps {
        echo '${project_title}'
        sh 'touch README.md'
        writeFile file: 'README.md', text: '''# Pipeline Practice

        This pipeline is a practice one.'''
        
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