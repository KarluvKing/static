    
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				withAWS(credentials:'IDofSystemCredentials') {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
			}
		}
	}
}
