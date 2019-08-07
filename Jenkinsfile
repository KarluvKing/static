pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(credentials:'IDofSystemCredentials', region:'eu-west-2') {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
			}
		}
	}
}
