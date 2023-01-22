node('JDK8') {
	stage('SourceCode') {
		// get the code from git repo
		git branch: 'sprint1_develop', url: 'https://github.com/techleads23/game-of-life.git'
	}

	stage('Build the code') {
		sh 'mvn clean package'
	}

	stage('Archiving and Test Results') {
		junit '**/surefire-reports/*.xml'
		archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	}
}
