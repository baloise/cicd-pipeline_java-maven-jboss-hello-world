@Library('sharedlib@2b33d8984171f6b216909eac7103d76c45985fa0') _
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