pipeline {
    agent any
    
    environment {
        NOMBRE = 'Eustaquio'
	MAQUINA = """${sh(
			returnStdout: true,
			script: 'uname -n'
			)
		}"""
    }

    stages {
        stage('Compile Simple') {
            steps {
                sh 'javac Simple.java'
            }
        }
        stage('Execute Simple') {
            steps {
                sh 'java Simple'
            }
        }
        stage('Compile Param') {
            steps {
                sh 'javac Param.java'
            }
        }
        stage('Execute Param') {
            steps {
                sh 'java Param ${NOMBRE}'
            }
        }
        stage('Machine') {
            steps {
                sh 'java Maquina ${MAQUINA}'
            }
        }
    }
}
