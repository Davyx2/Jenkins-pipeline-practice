node{
  def app
  stage('Clone') {
      checkout scm
  }

  stage('Build image') {
    sh 'docker build -t venance/nginx .'
  }

  stage('Run image') {
      
      sh 'docker run -d --name=nginx-dev -p 80:80 venance/nginx'

      sh 'docker ps'

      sh 'curl localhost'

  } 
  
}