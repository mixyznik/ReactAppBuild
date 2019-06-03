node {
  try {
    stage('pwd'){
      sh 'pwd'
      sh 'cd /'
      sh 'cd /home/mixy/pencil'
      sh 'pwd'
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