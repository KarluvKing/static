pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				sh 'echo "aqui 01"'
				withAWS(credentials:'IDofSystemCredentials', region:'eu-west-2') {
					sh 'echo "aqui 02"'
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
			}
		}
	}
}
