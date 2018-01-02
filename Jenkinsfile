pipeline {
  agent {
    label "jenkins-maven"
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow {
          cdOrganisation "jstrachan"
          cdBranches ['agent-label'] 
          disableGitPush true
          mavenProfiles ['no-artifact-repository'] 
          
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
