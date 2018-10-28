pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        sh '. env.sh'
        sh 'echo ${var1}'
        sh 'echo ${var2}'
        sh 'apk update'
        sh 'apk list vim'
      }
    }
  }
}
