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
                    sh 'git --no-pager diff origin/$CHANGE_TARGET --name-only'
                    def ret = sh(script: 'git --no-pager diff origin/$CHANGE_TARGET --name-only', returnStdout: true)
                    echo "${ret}"
                    
                    
                }                 
            }
        }
    }
}
