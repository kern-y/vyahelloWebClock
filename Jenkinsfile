pipeline {
    agent { 
        label 'master'
        }
    stages {
        stage('running a docker container') {
            steps {
                sh 'docker run -v /home/vm1kern/.jenkins/workspace/docker-image/clock:/usr/share/nginx/html:ro --name nginx_$BUILD_ID -d nginx '
                
            }
        }
    }
}
