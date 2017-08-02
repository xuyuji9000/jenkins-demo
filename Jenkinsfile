pipeline {
    agent { docker 'node:7-alpine' }
    stages {
        stage('Test') {
            steps {
                sh 'npm --version'
                sh 'echo $PATH'
            }
        }
    }
}
