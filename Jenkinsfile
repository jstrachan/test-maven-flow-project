pipeline {
  agent {
    label "jenkins-maven"
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow {
          cdOrganisation "jstrachan"
          disableGitPush true
          cdBranches(['agent-label']) 
          mavenProfiles(['no-artifact-repository']) 
          
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
