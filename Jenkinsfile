pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        build 'PES1UG22CS335-1'
        sh 'g++ main.cpp -o main1'
      }

    }
    stage('Test'){
      steps {
        sh './main1'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployed'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
