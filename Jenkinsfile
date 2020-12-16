pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8-alpine'
    }

  }
  stages {
    stage('Change directory') {
      steps {
        dir(path: 'express_example-master')
      }
    }

  }
  environment {
    HOME = '.'
  }
}