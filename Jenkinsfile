pipeline {
	agent any 
	
	stages {
		stage ('Checkout') {
			steps {
				checkout scm
			}
		}
		
		tools { maven 'Maven3' }  // name must match Manage Jenkins → Tools
		stage('Build and Test') {
			steps {
			    bat 'mvn -B clean test'
			}
		}

	}
}