node('JenkinsSlave') {
	stage('cleanup') {
		deleteDir()
	}
	stage('build') {
		bat 'git clone --recursive git@github.com:CommentViewerCollection/IPlugin.git'
		dir('./IPlugin') {
			bat '"C:\\Program Files (x86)\\Microsoft Visual Studio\\2017\\Community\\Common7\\Tools\\VsDevCmd.bat"'
			bat 'nuget restore IPlugin.sln'
			bat '"C:\\Program Files (x86)\\Microsoft Visual Studio\\2017\\Community\\MSBuild\\15.0\\Bin\\MSBuild.exe" IPlugin.sln'
		}
	}

	stage('test') {
	}
}
