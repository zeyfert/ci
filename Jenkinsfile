pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'python3 -m venv env'
                sh 'pwd'
                sh 'source ./env/bin/activate'
                sh 'sudo pip3 install -r requirements.txt'
                sh 'python app.py'
            }
        }
    }
}