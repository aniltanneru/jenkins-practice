pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECONDS')
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo Hello, This is Build'
                sh 'echo project: $PROJECT'
                sh 'echo "Hello ${params.PERSON}'
                sh 'echo "Biography: ${params.BIOGRAPHY}'
                sh 'echo "Toggle: ${params.TOGGLE}'
                sh 'echo "Choice: ${params.CHOICE}'
                sh 'echo "Password: ${params.PASSWORD}'
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