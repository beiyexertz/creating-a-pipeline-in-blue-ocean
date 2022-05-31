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

    stage('stage3') {
      steps {
        echo '123 message'
        sh 'ls -l'
      }
    }

    stage('stge4') {
      steps {
        echo 'end'
      }
    }

  }
  environment {
    a = 'b'
  }
}