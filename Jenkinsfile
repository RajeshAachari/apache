pipeline {
  agent any
  stages {
    stage('CHECKOUT') {
      parallel {
        stage('CHECKOUT') {
          steps {
            sh 'echo "stage 01"'
          }
        }

        stage('Worker') {
          steps {
            sh 'echo "stage of worker"'
          }
        }

      }
    }

    stage('BUILD') {
      steps {
        sh 'echo "stage of build"'
      }
    }

    stage('TEST') {
      parallel {
        stage('FIRSTFOX') {
          steps {
            sh 'echo "stage of test"'
            sh 'echo "stage of firefox"'
          }
        }

        stage('EDGE') {
          steps {
            sh 'echo "stage of edge programe"'
          }
        }

      }
    }

    stage('STAGING') {
      steps {
        sh 'echo "stage of staging"'
      }
    }

    stage('PRODUCTION') {
      steps {
        sh 'echo "stage of production control"'
      }
    }

  }
}