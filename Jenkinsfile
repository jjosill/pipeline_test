pipeline {
  agent any
  stages {
    stage('Build Assets') {
      agent any
      steps {
        echo 'Building Assets'
      }
    }
    stage('Trigger job') {
      agent any
      steps {
        build 'Job1'
      }
    }
    stage('Test') {
      agent any
      steps {
        echo 'Testing Artifacts...'
      }
    }
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
    stage('Deploy') {
      agent any
      steps {
        echo 'Deploy to aws or ssomething...'
      }
    }
  }
}
