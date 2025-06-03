pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/gthri2k/sample-pipeline.git'
      }
    }
    stage('Build') {
      steps {
        sh './build.sh'
      }
    }
    stage('Test') {
      steps {
        sh './test.sh'
      }
    }
    stage('Deploy') {
      steps {
        sh './deploy.sh'
      }
    }
  }
  post {
    success {
      echo '✅ Pipeline completed successfully.'
    }
    failure {
      echo '❌ Pipeline failed. Check the logs.'
    }
  }
}

