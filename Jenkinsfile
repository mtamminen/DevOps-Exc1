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
        sh 'chown -R 114:120 "/.npm"'
        sh 'npm install express_example-master'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

  }
}