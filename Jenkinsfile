pipeline {
	agent any
	stages {
		stage('Clone git') {
			steps{
				git branch: 'main', url: 'https://github.com/ducngovan/demo_jenkins.git'
			}
		}
		stage('Docker') {
			steps{
				withDockerRegistry(credentialsId: 'docker-hub', url: 'https://registry.hub.docker.com/') {
				sh 'docker build -t duc1996/demo_image:v2 .'
				sh 'docker push duc1996/demo_image:v2'
				}
			}
		}
	
	}
}