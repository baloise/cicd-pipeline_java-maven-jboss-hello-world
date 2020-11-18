@Library('sharedlib@5cae95b7d57d53d51c3206153fab8857540f3eb4') _
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
					mvn("package -DskipTests=true")				 
				}
			}
		}
    }
}