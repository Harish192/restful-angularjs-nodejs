pipeline {
    agent any
        stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
                sh 'node app.js
            }
        }
        stage('Deliver') { 
            steps {
                sh 'npm stop' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh 'npm start' 
            }
        }
    }
}
