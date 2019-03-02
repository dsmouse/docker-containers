pipeline {
  agent any
  stages {
    stage('build subsonic-stable') {
      steps {
        dir(path: 'subsonic-stable') {
          sh 'make build'
        }

      }
    }
    stage('docker1') {
      steps {
        sh '''docker image ls || true
docker container list || true'''
      }
    }
  }
}