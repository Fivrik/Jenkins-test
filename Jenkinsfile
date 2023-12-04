// Jenkinsfile (Declarative Pipeline)
pipeline {
  agent any // run on any available agent
  stages {
    stage('Install Maven') { // a stage for installing Maven
      steps {
        script {
          def mvnHome = tool name: 'apache-maven-3.6.1', type: 'maven' // get the Maven installation path
          env.PATH = "${mvnHome}/bin:${env.PATH}" // add Maven to the PATH environment variable
        }
      }
    }
    stage('Build') { // a stage for building the project
      steps {
        echo 'Building...' // print a message
        sh 'mvn clean package' // run a shell command to build with Maven
      }
    }
    stage('Test') { // a stage for testing the project
      steps {
        echo 'Testing...' // print a message
        sh 'mvn test' // run a shell command to test with Maven
      }
    }
    stage('Deploy') { // a stage for deploying the project
      steps {
        echo 'Deploying...' // print a message
        sh 'mvn deploy' // run a shell command to deploy with Maven
      }
    }
  }
}
