node ('master'){

	stage ('init'){
		a = {"val":1}
		if(a["val"] == 1){
			stage ('Print a = 1'){
				echo "Hello Hemanth"
			}
		} else {
			stage ('Print a = 2'){
				echo "Oye"
			}
		}

	}

	properties([[$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '3']]]);

}
