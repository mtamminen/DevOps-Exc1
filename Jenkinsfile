pipeline {
  agent {
    docker {
      image 'node:8-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        dir(path: 'express_example-master') {
          sh '''npm install
'''
        }

      }
    }

    stage('Test') {
      steps {
        dir(path: 'express_example-master') {
          sh 'npm test'
        }

      }
    }

  }
  environment {
    HOME = '.'
  }
}