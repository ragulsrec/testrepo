pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Code Checkout123'
        echo 'Compile'
        svn 'http://172.16.77.20/dmwirepo/Jenkins/cicd-modules/pipeline-scripts/trunk'
      }
    }
    stage('QualityCheck') {
      steps {
        echo 'Junit run'
        echo 'Sonar check'
      }
    }
    stage('D-Preparation') {
      steps {
        echo 'Scan cicd.properties'
        echo 'Checkout environment-resource'
        echo 'Checkout datasource-resource'
        echo 'Checkout lgiconfig-resource'
        echo 'Checkout messaging-resource'
      }
    }
    stage('D-Execution') {
      steps {
        echo 'Upload property files'
        echo 'Verify & Create softlinks'
        echo 'Verify & create datasource'
        echo 'Verify and create messaging configuration'
      }
    }
    stage('Deploy(D)') {
      steps {
        echo 'Verify and deploy the artifact'
      }
    }
    stage('Sanity') {
      steps {
        echo 'Execute modulewise sanity'
        echo 'Send email on results'
      }
    }
  }
  environment {
    build_path = 'http://172.16.77.20/dmwirepo/peal-api-2.0/trunk/peal-user-api'
  }
}