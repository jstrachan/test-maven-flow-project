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
          cdOrganisation: "jstrachan", 
          cdBranches: ['kubernetes-inherit-from'], 
          disableGitPush: true,
          mavenProfiles: ['no-artifact-repository'], 

          //pauseOnSuccess: "true", pauseOnFailure: "true",
        ) 
      }
    }
  }
}
