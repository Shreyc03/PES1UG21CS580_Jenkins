pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS580-1'
        sh 'g++ testJenkins.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
