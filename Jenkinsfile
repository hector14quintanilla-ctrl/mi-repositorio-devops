pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh "docker build -t mi-app-flask ./app"
            }
        }
        stage("Test") {
            steps {
                sh "docker run --rm mi-app-flask pytest"
            }
        }
        stage("Deploy") {
            steps {
                sh "docker-compose up -d --build"
            }
        }
    }
}
