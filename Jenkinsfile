// Checkout diretamente no S.O Windows

pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage ('Test') {
            steps {
                bat 'npm run test:ci'
            }
        }
		post {
			always {
				junit "logs/*.xml"
			}
		}
    }     
}