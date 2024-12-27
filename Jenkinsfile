pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'ls'
      }
    }

    stage('test') {
      steps {
        echo 'Hello Bro'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploy'
          }
        }

        stage('parallel') {
          steps {
            echo 'deploy last'
          }
        }

      }
    }

    stage('end') {
      parallel {
        stage('end') {
          steps {
            echo 'end'
          }
        }

        stage('deploy') {
          steps {
            echo 'hello'
          }
        }

      }
    }

  }
}