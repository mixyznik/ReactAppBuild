node {
  try {
    stage('pwd'){
      sh 'pwd'
      sh 'cd /'
      sh 'cd /home/mixy/pencil'
    }  
    stage('Checkout') {
      checkout scm
    }
    stage('Environment') {
      sh 'git --version'
      echo "Branch: ${env.BRANCH_NAME}"
      sh 'docker -v'
      sh 'printenv'
    }
  }
  catch (err) {
    throw err
  }
}