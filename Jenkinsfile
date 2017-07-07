node ('master'){
	
	stage ('Pull Git Repo'){
		git credentialsId: '242d8577-e4f4-4ff5-b4c0-6d65332bf8cf', url: 'https://github.com/jenkinsci/pipeline-plugin.git'		
	}

	stage ('Test'){
		sh '''cd $WORKSPACE
		ls -lart'''
	}

	properties([[$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '3']]]);

}
