pipeline {
	agent any 
	
	stages {
		stage ('Checkout') {
			steps {
				checkout scm
			}
		}
		
		tools { maven 'Maven_3' } 
		stage('Build and Test') {
			steps {
			    bat 'mvn -B clean test'
			}
		}

	}
}