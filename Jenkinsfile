pipeline {
    agent { 
        label 'master'
        }
    stages {
        stage('running a docker container') {
            steps {
                sh 'sudo docker run --name nginx8081 -d -p 8081:80 nginx'
                sh 'cd clock'
                sh 'sudo docker cp scripts styles clock.png index.html nginx8081:/usr/share/nginx/html'
            }
        }
    }
}
