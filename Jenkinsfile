pipeline {
  agent {
    label "fabric8-maven"
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow(
          cdOrganisation: "jstrachan", 
          cdBranches: ['master']
        ) {
          promoteArtifacts {
            pre {
              echo "====> hook invoked before promote artifacts!"
            }
          }
        }
      }
    }
  }
}
