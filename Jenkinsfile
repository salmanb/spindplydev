pipeline {
  agent any {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        sh 'apk update'
        sh 'apk list vim'
      }
    }
  }
}
