pipeline {
	agent any 
	
	stages {
		stages('Checkout') {
			steps {
				checkout scm
			}
		}
		
		stage ('Build and Test'){
			steps {
				sh 'mvn clean test package'
			}
		}
	}
}