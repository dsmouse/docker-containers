pipeline {
      agent any
            stages {
                    stage('build subsonic') {
                              steps {
                                          dir(path: 'subsonic') {
                                                        sh 'make build'
                                                                    }

                                                }
                                  }
                      }

}
