pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'building...'
      }
    }
    stage('test') {
      parallel {
        stage('chrome') {
          steps {
            echo 'first'
          }
        }
        stage('vivaldi') {
          steps {
            echo 'second'
          }
        }
      }
    }
    stage('deploy') {
      steps {
        echo 'deploying...'
      }
    }
  }
  environment {
    foo = 'bar'
  }
}