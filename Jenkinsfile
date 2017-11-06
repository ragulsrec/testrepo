pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'mvn clean install', returnStatus: true, returnStdout: true)
        bat(script: 'bat \'\'\'  echo "PATH = ${PATH}"', returnStatus: true, returnStdout: true)
      }
    }
  }
}