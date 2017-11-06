pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sh \'mvn clean install -Dmaven.test.failure.ignore=true\''
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