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

    stage('Build') {
      steps {
        tool 'gradle4'
        sh 'gradle build'
      }
    }

  }
  environment {
    COMPLETED_MSG = 'Build done!'
  }
}