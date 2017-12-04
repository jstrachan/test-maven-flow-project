pipeline {
  agent {
    label "fabric8-maven"
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
        ) 
      }
    }
  }
}
