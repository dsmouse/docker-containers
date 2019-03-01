pipeline {
  agent any
  stages {
    stage('Build Subsonic-stable') {
      steps {
        dir(path: 'subsonic-stable')
        sh 'docker build .'
      }
    }
  }
}