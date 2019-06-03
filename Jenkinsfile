node {
  try {
    stage('Checkout') {
      checkout scm
    }
    stage('Environment') {
      sh 'git --version'
      echo "Branch: ${env.BRANCH_NAME}"
      sh 'docker -v'
      sh 'printenv'
    }
    dir ('/home/mixy/pencil') {
    sh 'pwd'
    sh 'cp -R /home/qa/jenkins/workspace/pencil_master /home/mixy/pencil/'
    sh 'ls'
    }  
    stage('buils') {
      sh 'pwd'
     } 
    dir ('/home/mixy/pencil/pencil_master') {
       sh 'pwd'  
    }
  }
  catch (err) {
    throw err
  }
}