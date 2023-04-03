pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '''ls
pwd
touch files1'''
            echo 'Hello World'
          }
        }

        stage('Alert') {
          steps {
            echo 'THIS IS ALERT MESSAGE'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        sleep(unit: 'SECONDS', time: 10)
        echo 'This is Deploy'
      }
    }

  }
}