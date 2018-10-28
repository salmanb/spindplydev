pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        withEnv(["VAR1=${var1}", "VAR2=${var2}"]) {
          def result = sh(script: 'echo $VAR1; echo $VAR2')
          echo result
        }
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
}
