pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        sh '. env.sh'
        sh 'echo ${env.var1}'
        sh 'echo ${env.var2}'
        sh 'apk update'
        sh 'apk list vim'
      }
    }
  }
}
