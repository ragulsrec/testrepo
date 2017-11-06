pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'mvn install', returnStatus: true, returnStdout: true)
      }
    }
  }
}