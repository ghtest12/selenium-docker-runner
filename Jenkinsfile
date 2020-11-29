pipeline {
	agent any
	stages{
		stage("Start Grid"){
			sh "docker-compose up -d hub chrome firefox"
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up contactusverification.xml checklinksonhome.xml"
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}
