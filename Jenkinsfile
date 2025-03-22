pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/dariocaberlotto/testapp'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh "docker build -t dariocaberlotto/testapp:${env.BUILD_NUMBER} ."
                }
            }
        }
        stage('Test') {
            steps {
                sh "docker run --rm dariocaberlotto/testapp:${env.BUILD_NUMBER} ./run-tests.sh"
            }
        }
    }
}