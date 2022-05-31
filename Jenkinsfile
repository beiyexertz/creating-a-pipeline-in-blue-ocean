pipeline {
  agent any
  stages {
    stage('abc') {
      parallel {
        stage('abc') {
          steps {
            sh 'echo "abc"'
          }
        }

        stage('stage2') {
          steps {
            sleep 20
            zip(zipFile: 'a', dir: 'b', exclude: 'c', file: 'd', glob: 'd')
          }
        }

      }
    }

  }
  environment {
    a = 'b'
  }
}