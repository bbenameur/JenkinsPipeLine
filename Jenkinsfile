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
            echo '"Get the DriverPath ${ChromeDriverPath}"'
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
  environment {
    ChromeDriverPath = '/labs/chrome'
  }
}