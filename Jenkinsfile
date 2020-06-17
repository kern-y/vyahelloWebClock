pipeline {
    agent { 
        label 'master'
        }
    stages {
        stage('running a docker container') {
            steps {
                sh 'docker run --name nginx8081 -d -p 8081:80 nginx'
                sh 'cd clock'
                sh 'docker cp scripts nginx8080:/usr/share/nginx/html'
                sh 'docker cp styles nginx8080:/usr/share/nginx/html'
                sh 'docker cp clock.png nginx8080:/usr/share/nginx/html'
                sh 'docker cp index.html nginx8080:/usr/share/nginx/html'
            }
        }
    }
}
