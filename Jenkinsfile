pipeline {
	agent any
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}
