pipeline {
    agent {
        docker { image 'python' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'print("Hello") > app.py'
                sh 'python app.py'
                // sh 'source ./env/bin/activate'
                // sh './env/bin/python -m pip install -r requirements.txt'
                // sh './env/bin/python app.py'
            }
        }
    }
}