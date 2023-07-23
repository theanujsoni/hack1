pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // This step checks out the code from your repository
                // Make sure to configure your repository URL in the Jenkins project
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // This step installs the Node.js dependencies using npm or yarn
                sh 'npm install' // or 'yarn install'
            }
        }
        
        stage('Run Tests') {
            steps {
                // If you have automated tests for your JavaScript code, run them here
                // For example, if you're using npm, you might run: 'npm test'
                // If you don't have tests, you can skip this stage
                sh 'npm test'
            }
        }
        
        stage('Build') {
            steps {
                // This step builds your JavaScript project
                // For example, if you're using npm, you might run: 'npm run build'
                sh 'npm run build'
            }
        }
    }
}
