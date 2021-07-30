pipeline{
	agent any
	stages{
		stage("Pull lastest Image"){
			steps{
				bat "docker pull jorgedelgado93/selenium-docker"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
				bat "docker-compose ps"
				bat "docker-compose up selenium-docker selenium-docker2"
			}	
		}
		stage("Bring Grid Down"){
			steps{
				bat "docker-compose down"
			}
		}
	}
}
