pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Code Checkout'
        echo 'Compile'
        echo 'Update JIRA on compile status'
      }
    }
    stage('QualityCheck') {
      steps {
        echo 'Junit run'
        echo 'Sonar check'
        echo 'Update JIRA on junit  status and attach sonar reports'
      }
    }
    stage('Deploy-Prepare') {
      steps {
        echo 'Scan cicd.properties'
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
        echo 'Verify & create datasource'
        echo 'Verify and create messaging configuration'
        echo 'Verify and Deploy on IT environment'
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
    stage('Release') {
      steps {
        echo 'Release artifact to nexus'
        echo 'Update JIRA on release details'
        echo 'Send email on release details'
      }
    }
  }
}