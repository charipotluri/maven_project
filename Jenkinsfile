// Powered by Infostretch 

timestamps {

node () {

	stage ('test - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/charipotluri/maven_project.git']]]) 
	}
	stage ('test - Build') {
 			// Maven build step
	withMaven(maven: 'maven') { 
 			if(isUnix()) {
 				sh "mvn package " 
			} else { 
 				bat "mvn package " 
			} 
 		} 
	}
}
}
