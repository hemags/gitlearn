node ('master'){
	
	stage ('Pull Git Repo'){
		git credentialsId: '242d8577-e4f4-4ff5-b4c0-6d65332bf8cf', url: 'https://github.com/hemags/gitlearn.git'		
	}

	stage ('Test'){
		sh '''cd $WORKSPACE
		ls -lart'''
	}

	stage ('JIRA value'){
		jiraSearch 'project = HC AND issuetype = "New Cluster" AND status = Open AND resolution = Unresolved AND comment ~ "approved"'
	}

	properties([[$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '3']]]);

}
