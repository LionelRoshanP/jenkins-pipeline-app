pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/LionelRoshanP/jenkins-pipeline-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Start Web App') {
            steps {
                bat 'start /B python app.py'
                sleep 5
            }
        }
        stage('Ping App') {
            steps {
                bat 'curl -I http://localhost:5000'
            }
        }
    }
}
