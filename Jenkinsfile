pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:10-alpine'
    }

  }
  stages {
    stage('Run') {
      steps {
        sh 'ng serve'
      }
    }
  }
}