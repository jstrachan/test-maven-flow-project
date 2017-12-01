pipeline {
  agent {
    kubernetes {
      podTemplate {
        inheritFrom "fabric8-maven"
      }
    }
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow(
          cdOrganisation: "jstrachan", 
          cdBranches: ['master'], 
          pauseOnSuccess: "true", 
          pauseOnFailure: "true",
        ) 
      }
    }
  }
}
