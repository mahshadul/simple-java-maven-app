pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3002:3002'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        cleanWs(cleanWhenAborted: true)
      }
    }
    stage('del') {
      steps {
        input(message: 'hie', id: 'test')
      }
    }
  }
}