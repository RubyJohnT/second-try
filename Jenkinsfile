pipeline {
    agent { node {label 'labelName'} docker { image 'golang' } }
    stages {
        stage('build') {
            steps {
                sh 'golint ./...'
            }
        }
    }
}
