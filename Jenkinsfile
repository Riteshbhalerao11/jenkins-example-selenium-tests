pipeline {
  agent any
  stages {
    stage('Verify browsers are installed') {
      steps {
        bat 'wmic datafile where name="C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe" get Version /value'
      }
    }
    stage('Run Tests') {
      steps {
        bat './mvnw clean test'
      }
    }
  }
}