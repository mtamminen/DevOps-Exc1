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
        sh 'npm --prefix DevOps-Exc1_Development test'
      }
    }

  }
  environment {
    HOME = '.'
  }
}