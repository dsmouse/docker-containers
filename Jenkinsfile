pipeline {
  agent any
  stages {
    stage('build subsonic-stable') {
      steps {
        dir(path: 'subsonic-stable') {
          sh 'docker build .'
        }

      }
    }
  }
}