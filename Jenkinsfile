//scripted 
//declrative

pipeline {
       // agent any
	   agent {docker {image 'maven:3.6.3'}}
		stages{
			stage('Build'){
				steps{
					sh 'mvn --version'
					echo "Build"
				}
			}
			stage('Test'){
				steps{
					echo "Test"	
				}
			}
			stage('Integration Test'){
				steps{
					echo "Integration Test"	
				}
			}
		}
		post{
			always{
				echo "i run always"
			}
			success{
				echo "i run when success"
			}
			failure{
				echo "i run when you failied"
			}
		}
		
}
