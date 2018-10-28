node {
  stage ("git checkout") {
    checkout scm
  }
  stage("docker stuff") {
    load 'env.sh'
    withEnv(["VAR1=${var1}"]) {
      def result = sh(script: 'echo $VAR1', returnStdout: true)
      echo result
    }
    docker.image("alpine:latest").withRun(-e "CMD_1=$VAR1") { c ->
     sh "apk update"
     sh "apk list vim" 
    }
  }
}
/** pipeline {
  agent {
    docker { image "alpine:latest" }
  }
  stages {
    stage("first") {
      steps {
        load "env.sh"
        withEnv(["VAR1=${var1}",
             "VAR2=${var2}"
            ]) {
        def result = sh(script: 'echo $VAR1; echo $VAR2', returnStdout: true)
        echo result
    }
        sh "apk update"
        sh "apk list vim"
      }
    }
  }
} **/
