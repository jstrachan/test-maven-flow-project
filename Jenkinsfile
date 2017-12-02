pipeline {
  agent {
    kubernetes {
      label "fabric8-maven"
      inheritFrom "fabric8-maven"
    }
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow(
          //pauseOnSuccess: "true", pauseOnFailure: "true",

          cdOrganisation: "jstrachan", 
          cdBranches: ['kubernetes-inherit-from'], 
          disableGitPush: true,
          mavenProfiles: ['no-artifact-repository'] 
        ) 
      }
    }
  }
}
