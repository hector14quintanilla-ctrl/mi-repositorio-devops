pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                bat "docker build -t mi-app-flask ./app"
            }
        }
        stage("Deploy") {
            steps {
                bat "docker-compose up -d --build"
            }
        }
    }
}
