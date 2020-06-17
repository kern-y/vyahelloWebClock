pipeline {
    agent { 
        label 'master'
        }
    stages {
        stage('running a docker container') {
            steps {
                sh 'docker run --name nginx8080 -d -p 8081:80 nginx'
                sh 'cd clock'
                sh 'docker cp scripts styles clock.png index.html nginx8081:/usr/share/nginx/html'
            }
        }
    }
}
