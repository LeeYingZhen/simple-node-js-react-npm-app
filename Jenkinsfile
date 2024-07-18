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
	stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
        // Add more stages as needed
    }
}