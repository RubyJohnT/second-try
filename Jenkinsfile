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
                    
                    
                    def full_string = "/var/x /var/y /var/z"
                    def arr = full_string.split(" ")
                    for (i in arr) {
                      println "now got ${i}"
                    }
                }                 
            }
        }
    }
}
