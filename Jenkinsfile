pipeline {
  agent any
  stages {
    stage('build subsonic-stable') {
      parallel {
        stage('build subsonic-stable') {
          steps {
            dir(path: 'subsonic-stable') {
              sh '''export TAG_NAME=${BRANCH_NAME}
export APP_REPO=dsmouse.net
make build'''
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
    stage('docker1') {
      steps {
        sh '''docker image ls || true
docker container list || true
date'''
      }
    }
  }
}