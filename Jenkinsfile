pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'teststep'
          }
        }

        stage('test par') {
          steps {
            echo 'testpar'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 30
      }
    }

  }
}