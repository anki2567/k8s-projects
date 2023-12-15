pipeline {
	agent any
	
		
		// Define the maven tool
	
	stages {
		stage(' Build the source code using maven') {
			steps {
				sh 'mvn clean package'
			}
		}
		#Bulding docker image
		stage('Docker build') {
			steps {
				sh 'docker build  --t ankitha2001/java-app:1.4 .'
			}
		}
		
		
		
	}

}
