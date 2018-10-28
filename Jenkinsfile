node {
  stage("first") {
    sh 'echo hi'
    load 'env.sh'
    withEnv(["VAR1=${var1}"]) {
      def result = sh(script: 'echo $VAR1', returnStdout: true)
      echo result
    }
  }
}
