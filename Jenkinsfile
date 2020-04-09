pipeline {
  agent {
    docker {
      image 'itlinux/httpd-orange'
      args '-p 80:80'
    }
  }
  environment {
    CI = 'true'
  }
  stages {
    stage('Build') {
      steps {
        sh 'which bash'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/remo.sh'
      }
    }
  }
}
