node {
  def tasks = [:]
    stage("astage") {
      node {
        label 'master'
        def files = findFiles(glob: '*')
        for (int i = 0; i < files.size(); i++) {
          def filename = files[i]
          echo "${filename}"
          tasks["${filename}"] = {
              build job: 'paramproj', parameters: [ string(name: 'param1', value: "${filename}") ]
          }
        }
      }
    }
    stage("run parallel tasks") {
    parallel tasks
  }
}
