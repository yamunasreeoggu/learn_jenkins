pipeline {
  agent {
    node { label 'workstation' }
  }

  stages {

    stage('One') {
      steps {
        sh 'echo One'
      }
    }

    stage('Two') {
      steps {
        sh 'echo Two'
      }
    }
  }

  post {
    always {
      echo 'Sending Email'
    }
  }

}