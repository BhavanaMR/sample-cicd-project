pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Listing files in workspace:'
        sh 'ls -l'
        echo 'Running hello.sh script:'
        sh './hello.sh'
      }
    }
  }
  post {
    success {
      echo 'Pipeline completed successfully!'
    }
    failure {
      echo 'Pipeline failed.'
    }
  }
}
