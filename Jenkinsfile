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
			docker stop $(docker ps -aq) && docker rm $(docker ps -aq)
			docker compose up -d --build
			curl http://localhost:5000
			docker compose ps
			'''
                }
            }
        }
    }
}
