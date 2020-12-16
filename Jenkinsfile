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
        sh 'npm install express_example-master'
      }
    }

    stage('Test') {
      steps {
        dir(path: 'express_example-master/test') {
          sh 'npm test'
        }

      }
    }

  }
  environment {
    HOME = '.'
  }
}