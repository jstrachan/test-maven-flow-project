pipeline {
  agent {
    label "jx-maven"
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow(
          //pauseOnSuccess: "true", pauseOnFailure: "true",

          cdOrganisation: "jstrachan", 
          cdBranches: ['agent-label'], 
          disableGitPush: true,
          mavenProfiles: ['no-artifact-repository'] 
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
