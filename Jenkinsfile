pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/dariocaberlotto/testapp'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("dariocaberlotto/testapp:${env.BUILD_NUMBER}")
                }
            }
        }
    }
}