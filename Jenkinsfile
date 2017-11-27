pipeline {
  agent {
    kubernetes {
      label "fabric8-maven"
      podTemplateName "fabric8-maven"
    }
  }
  stages {
    stage('Maven Release') {
      steps {
        /*
        mavenFlow(pauseOnSuccess: "true") {
        }
        */
        mavenFlow(cdOrganisation: "jstrachan", cdBranches: ['pod-template-by-name']) {
        }
      }
    }
  }
}
