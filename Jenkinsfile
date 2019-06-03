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
    stage('Change dir') {
      steps {   
        dir ('/home/mixy/pencil') {
          sh 'pwd'
          sh 'cp -R /home/qa/jenkins/workspace/pencil_master /home/mixy/pencil/'
          sh 'ls'
        }

       } 
    } 
    
    stage('Change to pencil_master') {
       steps {  
        dir ('/home/mixy/pencil/pencil_master') {
          sh 'pwd'  
          sh 'npm install'
          sh 'screen -S pencil -d -m npm run start' 
          sh 'screen -ls'
          sh 'screen -X -S pencil quit'
          sh 'screen -ls' 
          sh 'npm run build'  
          sh 'cp -R /home/mixy/pencil/pencil_master/build/. /var/www/html/'
            }
        
      }
    }
  }
}