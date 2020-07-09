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
                    def files_list = sh(script: 'git --no-pager diff origin/$CHANGE_TARGET --name-only | grep ".go$"', returnStdout: true)
                    def arr = files_list.split("\n")
                    for (i in arr) {
                      sh 'golint -set_exit_status ${i}'
                    }
                }                 
            }
        }
    }
}
