pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        sh "env"
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
