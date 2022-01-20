properties([disableConcurrentBuilds()])

pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            // label 'test-app'
            additionalBuildArgs '--build-arg version=1.0.0 --tag test:123'
        }
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '1', artifactNumToKeepStr: '1'))
        timestamps ()
    }
    stages {
        stage('Build') {
            steps {
                // sh 'docker build .'
                deleteDir()
            }
        }
    }
}