pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello Word'
      }
    }
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
  }
}