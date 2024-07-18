pipeline {
    agent any
    tools {
        nodejs 'NodeJS 18' // Specify the Node.js installation name configured in Jenkins
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
	stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        // Add more stages as needed
    }
}