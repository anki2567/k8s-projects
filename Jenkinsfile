pipeline {
	agent any
	
		
		// Define the maven tool
	
	stages {
		stage(' Build the source code using maven') {
			steps {
				sh 'mvn clean package'
			}
		}
		
		stage('stage2') {
			steps {
				echo 'Hello world'
			}
		}
		
		
		
	}

}
