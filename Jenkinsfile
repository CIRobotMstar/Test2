pipeline {
  agent any
  stages {
    stage('') {
      steps {
        parallel(
          "Build_Code_ATSC": {
            sh 'echo \'Build ATSC\''
            
          },
          "Build_Code_DVB": {
            sh 'echo \'Build DVB\''
            
          },
          "Build_Code_ISDB": {
            build 'test'
            
          }
        )
      }
    }
    stage('Build_Result') {
      steps {
        sh 'echo \'test\''
      }
    }
    stage('Auto_Test') {
      steps {
        parallel(
          "Auto_Test_ATSC": {
            sh 'echo \'AT1\''
            
          },
          "Auto_Test_DVB": {
            sh 'echo \'AT2\''
            
          },
          "Auto_Test_ISDB": {
            sh 'echo \'AT3\''
            
          }
        )
      }
    }
    stage('Auto_Test_Result') {
      steps {
        sh 'echo \'end\''
      }
    }
  }
}