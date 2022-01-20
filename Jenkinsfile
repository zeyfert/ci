properties([disableConcurrentBuilds()])

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '1', artifactNumToKeepStr: '1'))
        timestamps ()
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build . --tag my-wep-app:1.0.0'
                deleteDir()
            }
        }
        stage('Push') {
            steps {
                sh 'docker push my-web-app docker-registry:5000/python/my-web-app:1.0.0'
            }
        }
    }
}