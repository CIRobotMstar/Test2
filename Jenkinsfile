pipeline {
  agent any
  stages {
    stage('') {
      steps {
        parallel(
          "Build": {
            sh 'echo \'Build\''
            
          },
          "Build2": {
            sh 'echo \'Build2\''
            
          },
          "Build3": {
            sh 'echo \'Build3\''
            
          },
          "Build4": {
            sh 'echo \'Build4\''
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        sh 'echo \'Test4\''
      }
    }
    stage('Print') {
      steps {
        echo 'End'
      }
    }
  }
  environment {
    source = '123'
  }
}