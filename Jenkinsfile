pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8-alpine'
    }

  }
  stages {
    stage('') {
      steps {
        dir(path: 'express_example-master') {
          sh 'npm install'
        }

      }
    }

  }
  environment {
    HOME = '.'
  }
}