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
        
      }
    }
    dir ('/home/mixy/pencil') {
        sh 'pwd'
        sh 'cp -R /home/qa/jenkins/workspace/pencil_master /home/mixy/pencil/'
        sh 'ls'
    }  

    dir ('/home/mixy/pencil/pencil_master') {
       sh 'pwd'  
    }
    stage('build app') {
      steps {  
        sh 'pwd'
        sh 'npm install'
      }
     } 
  }
}