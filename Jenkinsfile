pipeline {
	agent {  label 'linux-node1' }
	stages {
		stage('---clean---'){
			tools {
				maven 'maven3.8.6'
			}
			steps {
				
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'maven3.8.6'
			}
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			
			steps {
				
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was built successfully'
		}
		failure {
			echo 'job was not build..it was failure'
		}
	}
}
