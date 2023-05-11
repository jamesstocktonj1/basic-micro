pipeline {
    agent {
        docker { image 'golang:1.19.1-alpine' }
    }
    stages {
        stage('Pre-Test') {
            steps {
                sh 'go version'
            }
        }
        stage('Build') {
            steps {
                echo 'Compiling and building'
                sh 'go build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing Code'
                sh 'go test ./...'
            }
        }
    }
}