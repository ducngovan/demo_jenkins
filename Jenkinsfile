pipeline {
	agent any
	stages {
		stage('Clone git') {
			steps{
				git branch: 'main', url: 'https://github.com/ducngovan/demo_jenkins.git'
			}
		}
		stage('Clone build') {
			steps{
			echo 'Start docker................'
			sh 'run_app.sh'
			}
		}
	}
}