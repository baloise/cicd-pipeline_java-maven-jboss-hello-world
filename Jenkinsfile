@Library('sharedlib') _
pipeline {
    agent any

    options {
        disableConcurrentBuilds()
        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '15'))
    }

	
    stages {
		stage("Maven Build") {
			steps {
				echo(greet("private sunshine"))
				script {
					// TODO wrap this in a library call ( use docker container )
					// don't call sh directly
					sh "mvn package -DskipTests=true"
				}
			}
		}
    }
}