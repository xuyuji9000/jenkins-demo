pipeline {
    agent { docker 'node:carbon-alpine' }
    stages {
        stage('Test') {
            steps {
                sh 'echo $PATH'
            }
        }
    }
}
