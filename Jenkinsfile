@Library('sharedlib@cc41158e0a0728cd02a86868039edb095572d557') _
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