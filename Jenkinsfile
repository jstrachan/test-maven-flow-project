pipeline {
  agent {
    kubernetes {
      label "build-pod-mvn"
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
