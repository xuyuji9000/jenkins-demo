pipeline {
    agent { docker 'node:carbon-alpine' }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'ls'
            }
        }
    }
}
