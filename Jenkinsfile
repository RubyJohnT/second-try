pipeline {
    agent any
    tools {
        go 'go-1.11'
    }
    environment {
        GO111MODULE = 'on'
    }
    stages {
        stage('build') {
            steps {
                sh 'go version'
            }
        }
    }
}
