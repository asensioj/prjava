pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                sh 'javac Simple.java'
            }
        }
        stage('Execute') {
            steps {
                sh 'java Simple'
            }
        }
    }
}
