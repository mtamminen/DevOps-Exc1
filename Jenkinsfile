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
        sh 'npm install express_example_master/'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

  }
}