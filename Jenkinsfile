pipeline {
    agent any
    stages {
        stage('verify branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker image ls'
                sh 'docker build -t madhavi/nginx-image .'
                sh 'docker image ls'
            }
        }
    }
}
