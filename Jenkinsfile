pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:10-alpine'
    }

  }
  stages {
    stage('Restore') {
      steps {
        sh 'npm install'
      }
    }
  }
}