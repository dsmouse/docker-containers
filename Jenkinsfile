pipeline {
  agent any
  stages {
    stage('preenv') {
      steps {
        sh 'set'
      }
    }
    stage('Build') {
      steps {
        dir(path: 'subsonic-stable') {
          sh '''export TAG_NAME=${BRANCH_NAME}
export APP_REPO=dsmouse.net
make build'''
        }

      }
    }
    stage('postenv') {
      steps {
        sh '''date
set
docker container ls
docker images ls'''
      }
    }
  }
}