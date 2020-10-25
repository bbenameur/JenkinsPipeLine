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
            echo "Get the DriverPath ${ChromeDriverPath}"
          }
        }

        stage('Test Log') {
          steps {
            echo 'Test Log'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            input(message: 'Do you want to Deployment ?', id: 'OK')
            echo 'Deploying the app'
          }
        }

        stage('Artifacts') {
          steps {
           writeFile(file: 'LogTestFile.txt', text: "This is the ChromeDriverPath ${ChromeDriverPath} and localvariable Value ${LocalVariable}")
          }
        }

      }
    }

  }
  environment {
    ChromeDriverPath = '/labs/chrome'
  }
}
