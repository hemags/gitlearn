node ('master'){

	stage ('Print'){
		echo "Hello Hemanth"   
	}

	stage ('Pull Git Repo Code'){
		checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemags/gitlearn.git']]])
	}

}
