pipeline {
    agent any

    environment {
        COMPOSE_FILE = 'docker-compose.yml'
    }

    stages {
        stage('Build') {
            steps {
                script {
		checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'githubtoken', url: 'https://github.com/gustavoLadchuk/devops-docker-jenkins.git']])
                    sh '''
			docker-compose up -d --build
			'''
                }
            }
        }
    }
