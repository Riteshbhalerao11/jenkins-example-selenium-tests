pipeline {
  agent any
  stages {
    stage('Verify browsers are installed') {
      steps {
        bat 'google-chrome --version'
      }
    }
    stage('Run Tests') {
      steps {
        bat './mvnw clean test'
      }
    }
  }
}