pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'mvn clean install', returnStatus: true, returnStdout: true)
        echo 'Code Checkout'
      }
    }
    stage('Execute') {
      steps {
        bat(script: 'mvn spring-boot:run', returnStdout: true, returnStatus: true)
      }
    }
  }
}