properties([disableConcurrentBuilds()])

pipeline {
    agent {
        label 'master'
    }
    options {
        buildDiscarder(logRotator(numToKeep: '3', artifactNumToKeepStr: '1'))
        timestamps ()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Test'
                deleteDir()
            }
        }
    }
}