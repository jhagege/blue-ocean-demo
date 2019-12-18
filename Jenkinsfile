pipeline {
  agent {
    node {
      label 'docker-slave'
    }

  }
  stages {
    stage('Source') {
      steps {
        git 'https://github.com/explore-jenkins/blue-ocean-demo'
      }
    }

  }
  environment {
    COMPLETED_MSG = 'Build done!'
  }
}