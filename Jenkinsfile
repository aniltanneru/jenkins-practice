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
    post {
        always {
            echo 'I will always say Hello again!'
        }
        success {
            echo 'I will run when pipeline is success'
        }
        failure {
            echo 'I will run when pipeline is failed'
        }
    }
}