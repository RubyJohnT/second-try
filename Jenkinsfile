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
                for (changeLogSet in currentBuild.changeSets) { 
                    for (entry in changeLogSet.getItems()) { // for each commit in the detected changes
                        for (file in entry.getAffectedFiles()) {
                            sh 'golint -set_exit_status file.getPath()' // add changed file to list
                        }
                    }
                }
            }
        }
    }
}
