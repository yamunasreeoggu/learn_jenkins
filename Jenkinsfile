pipeline {
  agent {
    node { label 'workstation' }
  }

  environment {
    SAMPLE_URL = "https://sample.com"
    SSH = credentials("ssh")
    }

  options {
    ansiColor('xterm')
  }

  stages {

    stage('One') {
      steps {
        sh 'echo One'
        sh 'echo ${SAMPLE_URL}'
        sh 'echo $SSH'
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