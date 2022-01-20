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
                sh 'docker build . --tag docker-registry:5000/python/my-web-app:1.0.0'
                
            }
        }
        stage('Push') {
            steps {
                sh 'docker push docker-registry:5000/python/my-web-app:1.0.0'
            }
        }
        stage('Clean working directory') {
            steps {
                deleteDir()
            }
        }
    }
}