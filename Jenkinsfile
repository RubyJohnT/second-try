pipeline {
    agent any
    tools {
        go '1.13'
    }
    environment {
        GO111MODULE = 'on'
    }
    stages {
        stage('build') {
            steps {
                sh 'golint -set_exit_status ./...'
            }
        }
    }
}
