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
                scipt {
                    sh '/usr/local/bin/docker build -t testapp .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                scipt {
                    sh '/usr/local/bin/docker run -p 8090:80 testapp .'
                }
            }
        }
    }
}