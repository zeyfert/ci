pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'python3 -m venv env'
                sh 'pwd'
                sh 'source ./env/bin/activate'
                sh './env/bin/pip install -r requirements.txt'
                sh './env/bin/python app.py'
            }
        }
    }
}