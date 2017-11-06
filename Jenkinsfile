pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'bat \'mvn install\''
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}