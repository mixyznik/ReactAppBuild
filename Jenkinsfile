node {
  try {
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