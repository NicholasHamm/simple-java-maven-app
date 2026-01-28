pipeline {
  agent any

  tools {
    maven 'Maven_3'
    // jdk 'JDK21'
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build and Test') {
      steps {
        bat 'mvn -B -V clean test'
      }
    }
  }
	post {
	    always {
	      junit 'target/surefire-reports/*.xml'
	    }
	}
}
