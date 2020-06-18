pipeline {
    agent { 
        label 'master'
        }
    stages {
        stage("Pull repository") {
            steps {
				deleteDir() /* clean up our workspace */
                git(
					url: 'git@github.com:kern-y/vyahelloWebClock.git',
					credentialsId: 'github-ssh-key',
					branch: 'master'
				)
            }
        }
        stage('running a docker container') {
            steps {
                sh 'docker run -v /usr/share/nginx/html:/usr/share/nginx/html:ro --name nginx_$BUILD_ID -d nginx '
                
            }
        }
    }
}
