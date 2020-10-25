pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building The .Net Core APplication'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing The application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app'
      }
    }

  }
}