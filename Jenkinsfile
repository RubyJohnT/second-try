pipeline {
    agent { node {label 'labelName'} }
    stages {
        stage('build') {
            steps {
                sh 'golint ./...'
            }
        }
    }
}
