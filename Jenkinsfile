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
            retry(count: 5) {
              echo 'repeeat print'
            }

            task(name: 'abcde') {
              writeFile(file: 'a.txt', text: 't.txt', encoding: 'utf-8')
            }

          }
        }

      }
    }

    stage('stage3') {
      parallel {
        stage('stage3') {
          steps {
            echo '123 message'
            sh 'ls -l'
          }
        }

        stage('stage5') {
          steps {
            git(url: 'https://github.com/beiyexertz/creating-a-pipeline-in-blue-ocean.git', branch: 'master')
          }
        }

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