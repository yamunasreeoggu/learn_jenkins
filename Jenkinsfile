pipeline {
  agent {
    node { label 'workstation' }
  }

  environment {
    SAMPLE_URL = "https://sample.com"
    SSH = credentials("ssh")
    }

  stages {

    stage('One') {
      steps {
        sh 'echo One'
        sh 'echo ${SAMPLE_URL}'
        sh 'echo $ssh'
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