pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'source /etc/profile'
                sh 'node --version'
            }
        }
    }
}
