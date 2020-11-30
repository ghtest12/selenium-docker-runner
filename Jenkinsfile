pipeline {
	agent any
	stages{
		stage("Start Grid"){
			steps{
				//Use bat command in windows
				//sh "docker-compose up -d hub chrome firefox"
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				//Use bat command in windows
				//sh "docker-compose up contact-us home-links"
				bat "docker-compose up contact-us home-links"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'C:/Users/padal/Results/**'
			//Use bat command in windows
			//sh "docker-compose down"
			bat "docker-compose down"
		}
	}
}
