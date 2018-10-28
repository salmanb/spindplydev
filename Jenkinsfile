pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        sh "env"
        sh "echo ${var1}"
        sh "echo ${var2}"
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
