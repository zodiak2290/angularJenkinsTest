pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:10-alpine'
    }

  }
  stages {
    stage('INSTALANDO NPM') {
      parallel {
        stage('Clean npm') {
          steps {
            sh '''



npm cache clean --force'''
          }
        }
        stage('Install npm') {
          steps {
            sh 'npm install'
          }
        }
      }
    }
    stage('Install angular') {
      steps {
        sh '''npm install -g @angular/cli
'''
      }
    }
    stage('Build') {
      steps {
        sh 'ng build'
      }
    }
    stage('Run') {
      steps {
        sh 'pwd'
      }
    }
  }
}