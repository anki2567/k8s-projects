pipeline {
	agent any
	
		
		// Define the maven tool
	
	stages {
		stage(' Build the source code using maven') {
			steps {
				sh 'mvn clean package'
			}
		}
		
		stage('Docker build') {
			steps {
				sh 'docker build  -t ankitha2001/java-app:1.4 .'
			}
		}
		stage('push docker image to docker hub'){
			steps {
				withCredentials([usernamePassword(credentialsId: 'hub-credentials', passwordVariable: 'hubPwd', usernameVariable: 'hubUser')]) {
    			sh "docker login -u ${hubUser} -p ${hubPwd}"
			sh "docker push ankitha2001/java-app:1.4"		
					
}
			}
		    
		}
				
		
	}

}
