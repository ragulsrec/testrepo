pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Code Checkout123'
        echo 'Compile'
        input(message: 'Enter the module to be built', id: 'build_path')
        build(propagate: true, job: 'cicd-checkout')
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
}