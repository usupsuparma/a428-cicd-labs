pipeline {
    agent {
        docker {
            image 'node:16-buster-slim'
            args '-v /var/run/docker.sock:/var/run/docker.sock -p 3000:3000'
            env ['DOCKER_TLS_CERTDIR=/certs']
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}