pipeline {
  agent any
  environment {
    FOO = "foo"
  }
  stages {
    stage('Build') {
      steps {
        echo '${project_title}'
        sh 'touch README.md'
        writeFile file: 'README.md', text: '''# Pipeline Practice

        This pipeline is a practice one.'''
        
      }
      post {
        always {
          echo 'this step will always happen'
        }

        changed {
          echo 'this step will happen only if jenkins pipeline changed'
        }

        failure {
          echo 'this step will happen only if jenkins pipeline failed'
        }

        success {
          echo 'this step will happen only if jenkins pipeline succeed'
        }

        unstable {
          echo 'this step will happen only if jenkins pipeline unstable'
        }

        aborted {
          echo 'this step will happen only if jenkins pipeline aborted'
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