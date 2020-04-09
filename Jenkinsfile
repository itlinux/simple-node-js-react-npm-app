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
        sh 'ping -c 4 google.com'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
