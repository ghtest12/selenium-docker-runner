pipeline {
	agent any
	stages{
		stage("Start Grid"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up contact-us home-links"
			}
		}
		stage("Bring Grid Down"){
			steps{
				bat "docker-compose down"
			}
		}
	}
}
