pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'pipeline_vjrepo'
      }
    }
    stage('testing') {
      parallel {
        stage('testing') {
          steps {
            sh 'echo \'testing testing\''
          }
        }
        stage('Functional Testing ') {
          steps {
            sh 'echo "Functional Testing"'
          }
        }
      }
    }
    stage('Deploy QA ') {
      steps {
        sh 'echo " Deploy QA from testing"'
      }
    }
    stage('System Testing') {
      steps {
        sh 'echo \'system testing\''
      }
    }
    stage('prod') {
      steps {
        sh 'echo \'Prod\''
      }
    }
  }
}