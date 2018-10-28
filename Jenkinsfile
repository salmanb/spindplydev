pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        withEnv(["VAR1=${var1}", "VAR2=${var2}"])
        sh "echo $VAR1"
        sh "env"
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
