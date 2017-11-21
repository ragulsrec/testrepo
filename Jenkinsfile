pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Code Checkout : $build_path'
        echo 'Code Compile : $artifact_id'
        echo 'Update JIRA on compile status'
      }
    }
    stage('QualityCheck') {
      steps {
        echo 'Junit run'
        echo 'Sonar check'
        echo 'Update JIRA on junit status and attach sonar reports'
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
        echo 'Verify & Create datasource'
        echo 'Verify & Create messaging configuration'
        echo 'Verify & Deploy artifact'
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
  environment {
    build_path = 'http://172.16.77.20/dmwirepo/Jenkins/cicd-modules/datasource-resource/trunk'
    artifact_id = 'datasource-resource'
    environment = 'http://172.16.76.128:8001'
  }
}