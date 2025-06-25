pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '✅ Building the application...'
            }
        }

        stage('Deploy') {
            steps {
                sh 'nohup python3 app.py &'
            }
        }

        stage('Ping') {
            steps {
                sh './ping.sh'
            }
        }
    }
}