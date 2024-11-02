pipeline {
    agent any

    environment {
        COMPOSE_FILE = 'docker-compose.yml'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
			docker compose up -d --build
			docker compose ps
			'''
                }
            }
        }
    }
