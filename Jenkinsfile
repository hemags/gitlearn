
import groovy.json.JsonSlurperClassic 

@NonCPS
def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}

node ('master'){
	
	a = jsonParse('{"val":1}');

	stage ('init'){
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
