pipeline {
    agent {
        docker { image 'python' }
    }
    options { timestamps () }
    stages {
        stage('Build') {
            steps {
                sh 'python --version'
                deleteDir()
            }
        }
    }
}