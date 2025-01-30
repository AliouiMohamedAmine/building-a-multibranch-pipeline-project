pipeline {
    agent {
        docker {
            image 'node:16' // Use the official Node.js Docker image
            args '-u root' // Run as root to avoid permission issues
        }
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
    }
}
