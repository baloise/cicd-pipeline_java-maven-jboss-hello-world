pipeline {
    agent any

    options {
        disableConcurrentBuilds()
        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '15'))
    }

    stages {
        stage("Build") {
            steps {
              // Perform maven build and upload war-file to nexus here
            }
        }
    }
}