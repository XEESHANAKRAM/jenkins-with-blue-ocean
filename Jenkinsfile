pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh '''pwd
ls'''
      }
    }

    stage('test-deploy') {
      parallel {
        stage('test-deploy') {
          steps {
            echo 'Test deploy message'
          }
        }

        stage('test2-deploy') {
          steps {
            echo 'Hi paralel'
          }
        }

      }
    }

    stage('production') {
      steps {
        timeout(time: 5)
      }
    }

  }
}