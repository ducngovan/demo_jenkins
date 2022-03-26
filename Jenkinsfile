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
				withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
				sh 'docker build -t duc1996/demo_image:v3 .'
				sh 'docker push duc1996/demo_image:v3'
				}
			}
		}
	
	}
}