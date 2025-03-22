pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/dariocaberlotto/testapp'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'build -t testapp .'
                }
            }
        }
    }
}