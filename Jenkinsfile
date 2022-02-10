pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
        echo 'Hello world'
      }
    }

    stage('Test') {
      steps {
        mail(subject: 'Testing', body: 'Just for testing', cc: 'kayahuseyin64@gmail.com')
      }
    }

    stage('Deploy') {
      steps {
        mail(subject: 'final', body: 'message', cc: 'kayahuseyin64@gmail.com')
      }
    }

  }
}