pipeline {
  agent any
  stages {
    stage('build subsonic-stable') {
      parallel {
        stage('build subsonic-stable') {
          steps {
            dir(path: 'subsonic-stable') {
              sh 'make build'
            }

          }
        }
        stage('build subsonic') {
          steps {
            dir(path: 'subsonic') {
              sh 'true || make build'
            }

          }
        }
      }
    }
  }
}