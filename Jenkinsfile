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
				mvn("package -DskipTests=true")				 
				script {
				}
			}
		}
    }
}$