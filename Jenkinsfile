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
                    def changeLogSets = currentBuild.changeSets
                    for (changeLogSet in currentBuild.changeSets) { 
                        for (entry in changeLogSet.getItems()) { // for each commit in the detected changes
                            for (file in entry.getAffectedFiles()) {
                                def file = file.getPath() // add changed file to list
                            echo "  ${file}"
                            }
                        }
                     }
                }                 
            }
        }
    }
}
