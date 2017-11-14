pipeline {
  agent any
  stages {
    stage('Deploy-Prepare') {
      steps {
        echo 'Download EAR and Scan cicd.properties'
        echo 'Checkout environment-resource'
        echo 'Checkout datasource-resource'
        echo 'Checkout lgiconfig-resource'
        echo 'Checkout messaging-resource'
      }
    }
    stage('Deploy-Execution') {
      steps {
        echo 'Upload property files'
        echo 'Verify & Create softlinks'
        echo 'Verify & Create datasource'
        echo 'Verify & Create messaging configuration'
        echo 'Verify & Deploy to environment'
        echo 'Update JIRA on deployment status'
      }
    }
    stage('Sanity') {
      steps {
        echo 'Execute modulewise sanity'
        echo 'Send email on results'
        echo 'Update JIRA with sanity report'
      }
    }
  }
}