pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "compiling application"'
          }
        }

        stage('Unit Tests') {
          steps {
            bat 'echo "Running unit tests.."&& timeout 5'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        bat 'echo "Deploying to production server"'
      }
    }

  }
}