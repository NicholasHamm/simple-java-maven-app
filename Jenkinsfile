pipeline {
  agent any

  tools {
    maven 'Maven3'     // must match Manage Jenkins → Tools → Maven installations name
    // jdk 'JDK21'      // optional: only if you configured a JDK tool with this name
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
      post {
        always {
          junit 'target/surefire-reports/*.xml'
        }
      }
    }
  }
}
