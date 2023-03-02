pipeline {
  agent {
    docker {
      image 'node:lts-bullseye-slim'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Prueba') {
      environment {
        CI = 'true'
      }
      steps {
        sh './jenkins/scripts/test.sh '
      }
    }

  }
}