pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                // Si tu Jenkins esta en Windows usa bat, si esta en Linux/Docker usa sh
                sh "docker build -t mi-app-flask ./app"
            }
        }
        stage("Deploy") {
            steps {
                sh "docker-compose up -d --build"
            }
        }
    }
}
