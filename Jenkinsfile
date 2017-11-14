pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Code Checkout'
        echo 'Compile'
        echo 'Update JIRA'
      }
    }
    stage('QualityCheck') {
      steps {
        echo 'Junit run'
        echo 'Sonar check'
        echo 'Update JIRA with status and sonar reports'
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
        echo 'Verify and deploy artifact'
        echo 'Update JIRA on deployment status'
      }
    }
    stage('Sanity') {
      steps {
        echo 'Execute modulewise sanity'
        echo 'Send email on results'
        echo 'Update JIRA on build status'
      }
    }
  }
}