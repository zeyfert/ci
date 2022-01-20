properties([disableConcurrentBuilds()])

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '3', artifactNumToKeepStr: '1'))
        timestamps ()
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build .'
                deleteDir()
            }
        }
    }
}