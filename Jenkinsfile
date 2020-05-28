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
                pwsh(script: 'docker images ls')
                pwsh(script: """
                    docker images ls
                    docker build -t nginx-image .
                    docker images ls
                """)
            }
        }
    }
}
