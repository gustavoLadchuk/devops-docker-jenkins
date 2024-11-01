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
			echo "teste"
			docker-compose up -d --build
			'''
                }
            }
        }
    }
