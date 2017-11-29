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
          cdBranches: ['pod-template-by-name'], 

          //pauseOnSuccess: "true", pauseOnFailure: "true",
        ) 
      }
    }
  }
}
