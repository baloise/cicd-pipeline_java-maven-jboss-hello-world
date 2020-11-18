@Library('sharedlib@d960422127981eb8177313999adb1131607adae7') _
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