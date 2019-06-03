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
    dir ('/') {
    sh 'pwd'
    } 
    dir ('/home/mixy/pencil') {
    sh 'pwd'
    }   
    stage('pwd'){
      sh 'pwd'
    }
  }
  catch (err) {
    throw err
  }
}