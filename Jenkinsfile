pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        sh "echo $var1"
        sh "echo $var2"
        sh "env"
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
