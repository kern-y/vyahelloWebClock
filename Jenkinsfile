pipeline {
    agent {
        docker 'nginx'
    }
    stages {
        stage('Test') {
            steps {
                sh 'pwd'
                sh 'whoami'
            }
        }
    }
}
