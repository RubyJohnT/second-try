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
                script {
                    sh 'go get -u golang.org/x/lint/golint'
                    sh 'git branch'
                    def files = sh(script: 'git --no-pager diff origin/$CHANGE_TARGET --name-only | grep ".go$"', returnStdout: true)
                    def files_array = files.split("\n")
                    for (file in files_array) {
                      sh 'golint -set_exit_status ${file}'
                    }
                }                 
            }
        }
    }
}
