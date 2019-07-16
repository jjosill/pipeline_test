pipeline {
  agent any
  stages {
    stage('Build Assets') {
      parallel {
        stage('Build Assets') {
          agent any
          steps {
            echo 'Building Assets'
          }
        }
        stage('Trigger job') {
          steps {
            build 'Job1'
          }
        }
      }
    }
    stage('Test') {
      agent any
      steps {
        echo 'Testing Artifacts...'
      }
    }
    stage('Release') {
      parallel {
        stage('Release') {
          agent any
          steps {
            echo 'Release to production env...'
          }
        }
        stage('Testing') {
          steps {
            sh 'echo "Testing one last time"'
          }
        }
      }
    }
    stage('Deploy') {
      agent any
      steps {
        echo 'Deploy to aws or ssomething...'
      }
    }
  }
}