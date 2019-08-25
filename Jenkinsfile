pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:10-alpine'
    }

  }
  stages {
    stage('Restore') {
      parallel {
        stage('Restore') {
          steps {
            sh 'npm install'
          }
        }
        stage('Install NG') {
          steps {
            sh '''npm install -g @angular/cli
'''
          }
        }
      }
    }
  }
}