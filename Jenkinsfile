pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Source') {
      steps {
        git 'https://github.com/explore-jenkins/blue-ocean-demo'
      }
    }

    stage('Build') {
      steps {
        sh '${tool \'gradle4\'}/bin/gradle build'
      }
    }

  }
  environment {
    COMPLETED_MSG = 'Build done!'
  }
}