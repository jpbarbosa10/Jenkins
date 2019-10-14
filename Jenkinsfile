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
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-2',credentials:'f1f19d4f-ac4e-464a-8e45-7e7b21f9903e') {
          s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled:true, file:'index.html', bucket:'test-project-juan')
          }
      }
    }
  }
}