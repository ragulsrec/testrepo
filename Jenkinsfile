pipeline {

	tools {
		maven "Maven 3.3.9"
		jdk "Oracle JDK 8u40"
	}

	agent label:""

	stages {
		stage("build"){
		sh 'mvn clean install -Dmaven.test.failure.ignore=true"
		}		
		}
}