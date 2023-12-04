pipeline {
  agent any
  stages {
    stage('Install Maven') {
      steps {
        echo 'build'
      }
    }

    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
        sh 'mvn test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }

  }
}