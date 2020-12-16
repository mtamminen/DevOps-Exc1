pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        dir(path: 'express_example-master') {
          sh 'npm install'
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

    stage('Delivery') {
      steps {
        dir(path: 'express_example') {
          sh 'npm start'
        }

      }
    }

  }
  environment {
    HOME = '.'
  }
}