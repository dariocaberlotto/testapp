pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/dariocaberlotto/testapp'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t testapp .'
                }
            }
        }
    }
}