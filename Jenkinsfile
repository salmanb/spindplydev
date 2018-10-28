pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stage('build') {
    def someGroovyVar = 'Hello world'
    withEnv(['VAR1=VALUE ONE',
             "VAR2=${someGroovyVar}"
            ]) {
        def result = sh(script: 'echo $VAR1; echo $VAR2', returnStdout: true)
        echo result
    }
  }
}
