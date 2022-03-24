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
			sh 'docker build -t duc1996/demo_build_image:v1 -f Dockerfile . '
			}
		}
	}
}