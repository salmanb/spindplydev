pipeline {
  agent {
    docker { image "alpine:latest" }
  }

  withEnv(['VAR1=VALUE ONE',
  "VAR2=${someGroovyVar}"
  ]) {
    stage('build') {
      def someGroovyVar = 'Hello world'
      steps {
        sh "apk update"
        sh "apk list vim"
      }
    }
    def result = sh(script: 'echo $VAR1; echo $VAR2', returnStdout: true)
    echo result
  }
}
