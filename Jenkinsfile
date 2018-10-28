pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        withEnv(["VAR1=${var1}", "VAR2=${var2}"])
        sh "echo $VAR"
        sh "echo ${VAR2}"
        sh "env"
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
