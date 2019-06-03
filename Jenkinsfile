pipeline {
  agent any
 
  tools {nodejs "node"}
 
  stages {
    stage('Example') {
      steps {
        sh 'npm config ls'
      }
    }
    stage('Checkout') {
      steps {  
        checkout scm
      }
    }
    stage('Environment') {
      steps {  
        sh 'git --version'
        echo "Branch: ${env.BRANCH_NAME}"
        sh 'docker -v'
        sh 'printenv'
        sh 'npm install'
      }
    }
  }
}