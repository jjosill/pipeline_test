pipeline {
    agent any

    stages {
        stage('Build Assets') {
            agent any
            steps {
                echo 'Building Assets'
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
        stage('Deploy') {
            agent any
            steps {
                echo 'Deploy to aws or ssomething...'
            }
        }
    }
}
