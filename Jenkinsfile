pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'DOCKER_HOST="unix:///var/run/docker.sock" & docker-compose up -d --build'
            }
            post {
                success {
                    echo 'Build successful. Now archiving...'
                    
                }
            }
        }
    }
}
