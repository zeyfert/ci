pipeline {
    agent {
        docker { image 'python' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'whoami'
                sh 'python3 -m venv env'
                sh 'pwd'
                // sh 'source ./env/bin/activate'
                // sh './env/bin/python -m pip install -r requirements.txt'
                // sh './env/bin/python app.py'
            }
        }
    }
}