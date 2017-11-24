pipeline {
  agent {
    kubernetes {
      label "fabric8-maven"
    }
  }
  stages {
    stage('Maven Release') {
      steps {
        mavenFlow {
        }
      }
    }
  }
}
