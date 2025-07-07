pipeline {
    agent { label 'AGENT-1'}
    stages {
        stage('Build') {
            steps {
                sh 'echo Hello, This is Build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Hello, This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Hello, This is Deploy'
            }
        }
    }
}